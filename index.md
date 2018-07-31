
<html>
    <body>
        <script>
            if('geolocation' in navigator){

                // --- PEGANDO POSICIONAMENTO PELO NAVEGADOR DE FORMA ESTÁTICA
                // navigator.geolocation.getCurrentPosition(function(position){
                //     console.log(position)
                // })

                // --- PEGANDO POSICIONAMENTO PELO NAVEGADOR DE FORMA DINÂMICA
                const watcher = navigator.geolocation.watchPosition(function(position){
                console.log(position)
                }, function(error){
                    console.log(error)
                    // --- TER UM LOCALIZAÇÃO MAIS PRECISA A CADA 30 SEG. (30000)
                },{ enableHighAccuracy: true, maximumAge: 30000, timeout: 30000})

            }else{
                alert('Ops, Não foi Possível pegaar sua Localização');
            }
        </script>
    </body>
</html>
