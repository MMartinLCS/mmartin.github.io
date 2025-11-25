# mmartin.github.io

<html> 

<header class="header"><img class="py-4" src="https://www.druni.es/media/wysiwyg/logoStore/logo.svg" alt="Logo"> <!-- Puedes agregar aquí cualquier otro contenido del encabezado si es necesario --></header>
<div class="d-flex flex-column h-100 fixed-top">
    <div class="d-flex flex-column h-100 fixed-top">
        <div class="flex-shrink-0">
            <div class="container">
                <div id="lexcontainer"></div>
            </div>
        </div>
    </div>
</div>
<style>
  .bd-placeholder-img {
    font-size: 1.125rem;
    text-anchor: middle;
    -webkit-user-select: none;
    -moz-user-select: none;
    user-select: none;
}

@media (min-width: 768px) {
    .bd-placeholder-img-lg {
      font-size: 3.5rem;
  }
}
.header {
    height: 100px;
    border-bottom: 1px solid rgba(0,0,0,.3);
    display: flex;
    align-items: center;
    padding: 0 20px;
}

.header img {
    width: auto;
    height: 85%; /* Ajusta la altura de la imagen al alto del encabezado */
}

.footer {
    background-color: #000;
    color: white;
    padding: 10px 0;
    height: 80px;
}

.page-loader {
    pointer-events: auto !important;
}
</style>

<script type="text/javascript">
    function loadScript(url, callback){
        var script = document.createElement('script');
        script.type = 'text/javascript';

        script.onload = function(){
            callback();
        };

        script.onerror = function() {
            console.error('Error on load library:', url);
        };

        script.src = url;
        document.getElementsByTagName('head')[0].appendChild(script);
    }

    loadScript('https://druni.lightning.force.com/lightning/lightning.out.js', function(){
        console.log('Library lightning.out.js loaded.');

        $Lightning.use("c:embeddedCaseFormWebApp",
            function() {
                console.log('Agregar componente.');
                $Lightning.createComponent(
                    "c:embeddedCaseFormWeb",
                    {},
                    "lexcontainer",
                    function(cmp) {
                        console.log('Inicializado.');
                    }
                    );
            },
            'https://druni.my.salesforce-sites.com/casoWeb'
            );
    });
</script>
  
</html>
