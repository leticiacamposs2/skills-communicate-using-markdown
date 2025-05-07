# Cabeçalho h1

## Cabeçalho h2

### Cabeçalho h3

#### Cabeçalho h4

##### Cabeçalho h5

###### Cabeçalho h6

Teste de imagem

![Image of Sponsortocat](https://octodex.github.com/images/sponsortocat.png)

Exemplo de código

```javascript
// Função que converte texto Markdown simples em HTML
function convertMarkdownToHtml(markdown) {
  // Substitui títulos (## Título -> <h2>Título</h2>)
  let html = markdown.replace(/^## (.*$)/gim, '<h2>$1</h2>');
  
  // Substitui subtítulos (# Título -> <h1>Título</h1>)
  html = html.replace(/^# (.*$)/gim, '<h1>$1</h1>');
  
  // Substitui texto em negrito (**texto** -> <b>texto</b>)
  html = html.replace(/\*\*(.*)\*\*/gim, '<b>$1</b>');
  
  // Substitui texto em itálico (*texto* -> <i>texto</i>)
  html = html.replace(/\*(.*)\*/gim, '<i>$1</i>');
  
  // Substitui links ([texto](url) -> <a href="url">texto</a>)
  html = html.replace(/\[(.*?)\]\((.*?)\)/gim, '<a href="$2">$1</a>');
  
  return html.trim(); // Remove espaços desnecessários
}

// Exemplo de uso
const markdownText = `
# Bem-vindo ao Markdown
## Markdown é simples!
Você pode usar **negrito**, *itálico*, e links como [este exemplo](https://github.com).
`;

const htmlOutput = convertMarkdownToHtml(markdownText);
console.log(htmlOutput);
```
