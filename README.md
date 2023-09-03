# Intel-laf
proyecto realizado para el curso de desarrollo web en Coderhouse, tineda online de productos electronicos, gaming, y accesorios.

###### Temas aplicados:
- Html
- Css
- Box-Model
- Flex-Box
- Grid
- Sass
- Seo

## Farmework [Bootstrap](http://https://getbootstrap.com/ "Bootstrap")
![](https://getbootstrap.com/docs/5.3/assets/brand/bootstrap-logo-shadow.png)

###### Install via package manager
Instale los archivos fuente Sass y JavaScript de Bootstrap a través de npm, RubyGems, Composer o Meteor. Las instalaciones administradas por paquetes no incluyen documentación ni nuestros scripts de compilación completos.

`npm install bootstrap@5.3.1`

`gem install bootstrap -v 5.3.1`

###### Include via CDN
Cuando solo necesite incluir CSS o JS compilado de Bootstrap, puede usar jsDelivr. Véalo en acción con nuestro sencillo inicio rápido o explore los ejemplos para impulsar su próximo proyecto. También puedes optar por incluir Popper y nuestro JS por separado.

`<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-4bw+/aepP/YC94hEpVNVgiZdgIC5+VKNBQNGCHeKRQN+PtmoHDEXuppvnDJzQIu9" crossorigin="anonymous">`

`<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/js/bootstrap.bundle.min.js" integrity="sha384-HwwvtgBNo3bZJJLYd8oVXjrBZt8cqVSpeBNS5n7C8IVInixGAoxmnlMuBnhbgrkm" crossorigin="anonymous"></script>`

###### Icon [Font Awesome](http://https://fontawesome.com/ "Font Awesome")


## Css Grid Responsive
Para evitar el uso eccesivo de media queries y tener un codigo mas limpio y legible, usonado solo 3 lineas de codigo

###### Responsive con media queries:
    .gallery {
        display: grid;
        min-width: 12rem;
        overflow: hidden;
        margin-right: 1rem;
        gap: 1rem;
        grid-auto-columns: 5rem;
        grid-auto-flow: column;
        grid-template-columns: 1fr;
    }
    
    @media screen and (max-width:40rem){
        .gallery {
            grid-template-columns: repeat(2, 1fr);
        }
    }
    
    @media screen and (max-width:58rem){
        .gallery {
            grid-template-columns: repeat(3, 1fr);
        }
    }
    
    @media screen and (max-width:70rem){
        .gallery {
            grid-template-columns: repeat(4, 1fr);
        }
    }
    
    @media screen and (max-width:78rem){
        .gallery {
            grid-template-columns: repeat(5, 1fr);
        }
    }

###### Utilizando Grid responsive:
    el auto-fill rellena la fila con columnas aun que estas queden vacias
	
    .gallery {
        display: grid;
        grid-template-columns: repeat(auto-fill minmax(40rem, 1fr));
        grid-auto-rows: 30rem;
    }
	
    el auto-fit permite expandir las columnas para llenar la fila
	  
    .gallery {
        display: grid;
        grid-template-columns: repeat(auto-fit minmax(40rem, 1fr));
        grid-auto-rows: 30rem;
    }

    la funcion minmax() solo es permitido en Grid
