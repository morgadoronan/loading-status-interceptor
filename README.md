# loading-status-interceptor

## Instalação

Inclua os arquivos abaixo na sua página
```html
<!--angularjs scripts/modules -->
<link href="<%=ResolveUrl("~/")%>UAUComponente/lib/loadingStatusStyle.css" rel="stylesheet" />
<script src="<%=ResolveUrl("~/")%>UAUComponente/lib/loadingStatusDirective.js"></script>
```


Adicione uma div a pagina utilizando a diretiva `loading-status-message`
```html
<div loading-status-message time-request="30" class="modal" style="position:fixed; display:none;">Aguarde...</div>
```
Para cada pagina do UauWeb é recomendado ter uma camada de serviços. É necessário injetar no serviço que deve ser interceptado a seguinte  dependência `loadingStatus`
```javascript
var appService = angular.module('myService', ['restangular', 'loadingStatus']);
```

Adicionar a seguinte configuração no serviço a ser interceptado
```javascript
    appService.config(function (RestangularProvider) {
        //set the base url for api calls on our RESTful services
        RestangularProvider.setDefaultHeaders({ 'intercept': true });
    });
```

### Attributes

| option | description | value | default |
|---|---|---|---|
| `close-on-select` | Closes a multi-select upon selection | boolean | true |
