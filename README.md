# Integração Iframe – Galaxies Survey

Este guia mostra como embutir o formulário da Galaxies no seu site usando um `<iframe>` responsivo, seguro e otimizado.

---

## 🔗 URL do Formulário

Use o link da pesquisa fornecido:

**https://app.galaxies.gg/survey/6812a81a0ebb69d258dceaed**

### Parametros

| Parâmetro    | Exemplo                      | Descrição                                  |
| ------------ | ---------------------------- | ------------------------------------------ |
| `sourcePath` | `?sourcePath=meusite.com.br` | Identificador da origem do acesso          |
| `email`      | `&email=usuario@email.com`   | Preenche automaticamente o campo de e-mail |

---

## ✅ Implementação Iframe Survey Básico sem parametros

### Copie o HTML básico

Cole este código onde deseja que o formulário apareça:

```html
<iframe
  src="https://app.galaxies.gg/survey/6812a81a0ebb69d258dceaed"
  title="Formulário Galaxies"
  allowfullscreen
  loading="lazy"
  sandbox="allow-scripts allow-same-origin allow-forms"
  style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;"
>
</iframe>
```

## ✅ Implementação Iframe Survey com parametros

### Exemplo fixo (URL direta):

```html
<iframe
  src="https://app.galaxies.gg/survey/6812a81a0ebb69d258dceaed?sourcePath=meusite.com.br&email=teste@exemplo.com"
  title="Formulário Galaxies"
  allowfullscreen
  loading="lazy"
  sandbox="allow-scripts allow-same-origin allow-forms"
  style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;">
</iframe>

```

### Ou via script (exemplo com preenchimento automático):
```javascript 
  const email = 'usuario@dominio.com';
  const origem = window.location.hostname;
  
  const iframe = document.createElement('iframe');
  iframe.src = `https://app.galaxies.gg/survey/6812a81a0ebb69d258dceaed?sourcePath=${origem}&email=${encodeURIComponent(email)}`;
  iframe.style = "position:absolute;top:0;left:0;width:100%;height:100%;border:0;";
  iframe.setAttribute("allowfullscreen", "");
  iframe.setAttribute("loading", "lazy");
  iframe.setAttribute("sandbox", "allow-scripts allow-same-origin allow-forms");
  
  document.getElementById('iframe-container').appendChild(iframe);

```


