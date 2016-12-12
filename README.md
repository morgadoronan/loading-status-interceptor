# loading-status-interceptor

## Instalação

Inclua os arquivos abaixo na sua página

```html
<!--angularjs scripts/modules -->
<link href="<%=ResolveUrl("~/")%>UAUComponente/lib/loadingStatusStyle.css" rel="stylesheet" />
<script src="<%=ResolveUrl("~/")%>UAUComponente/lib/loadingStatusDirective.js"></script>

Adicione uma div a pagina utilizando a diretiva `loading-status-message`

```
<div loading-status-message time-request="30" class="modal" style="position:fixed; display:none;">Aguarde...</div>
```
