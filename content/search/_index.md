---
title: "Paieška"
date: 2020-12-23T17:08:09+02:00
draft: false
---

{{< rawhtml >}}

<div class='row searchrow'>
<p>Suveskite vieną žodį arba frazę ir paspauskite Enter</p><br><br>
<input type='text' class='searchBar form-control form-control-lg' placeholder='Ko ieškote?' style='width:100%;height:40px;'/>
</div>
<script>
    window.addEventListener('load',()=>{
        let selectedField = document.querySelector('.searchBar');
        let selectedRow = document.querySelector('.searchrow');
        let mas;

        selectedField.addEventListener('keyup',(k)=>{
            if(k.key=="Enter" || k.keyCode===13){
                let fieldValue = selectedField.value;
                selectedRow.innerHTML = "Ieškoma...";
                let siteBase = window.location.origin;
                let siteUrl = window.location.href;
                let rssUrl = siteBase+"/sitemap.xml";
                let found = false;
                fetch(rssUrl).then(response=>response.text()).
                then(str=>new window.DOMParser().parseFromString(str,"text/xml")).
                then((data)=>{
                    mas = data.getElementsByTagName('item');
                    selectedRow.innerHTML = '';
                    for(let index=0;index<mas.length;index++){
                        if(mas[index].getElementsByTagName('description')[0].textContent.toLowerCase().includes(fieldValue.toLowerCase())){
                            if(mas[index].getElementsByTagName('link')[0].textContent!=siteUrl){
  selectedRow.innerHTML+="<div class='col-lg-8 col-md-8 col-sm-12 col-xs-12 mx-auto mt-2 mb-2'><p><h2 class='card-title'>"+mas[index].getElementsByTagName('title')[0].textContent+"</h2></p><p>"+mas[index].getElementsByTagName('description')[0].textContent.substring(0,300)+"...</p><p><a class='btn btn-md btn-dark' href='"+mas[index].getElementsByTagName('link')[0].textContent+"'>"+mas[index].getElementsByTagName('link')[0].textContent+"</a></p></div><br><br>";
                            found = true;
                            }
                        }
                      

                    }
                    if(found === false){
                         selectedRow.innerHTML = '';
                         selectedRow.innerHTML = '<p>Įrašų nerasta</p>';
                    }
                  
                })
}


            
        })
    })
</script>
{{< /rawhtml >}}
