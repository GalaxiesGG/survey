# Iframe Integration – Galaxies Survey

This guide shows how to embed the Galaxies form on your site using a responsive, secure, and optimized `<iframe>`.

---

## 🔗 Form URL

Use the provided survey link:

**https://app.galaxies.gg/survey/6812a81a0ebb69d258dceaed**

### Parameters

| Parameter    | Example                          | Description                                  |
| ------------ | -------------------------------- | -------------------------------------------- |
| `sourcePath` | `?sourcePath=mywebsite.com`      | Identifier of the access origin              |
| `email`      | `&email=user@email.com`          | Automatically fills in the email field       |

---

## ✅ Basic Iframe Survey Implementation without parameters

### Copy the basic HTML

Paste this code where you want the form to appear:

```html
<iframe
  src="https://app.galaxies.gg/survey/6812a81a0ebb69d258dceaed"
  title="Galaxies Form"
  allowfullscreen
  loading="lazy"
  sandbox="allow-scripts allow-same-origin allow-forms"
  style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;"
>
</iframe>
```

## ✅ Iframe Survey Implementation with parameters

### Fixed example (direct URL):

```html
<iframe
  src="https://app.galaxies.gg/survey/6812a81a0ebb69d258dceaed?sourcePath=meusite.com.br&email=test@email.com"
  title="Formulário Galaxies"
  allowfullscreen
  loading="lazy"
  sandbox="allow-scripts allow-same-origin allow-forms"
  style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;">
</iframe>

```

### Or via script (example with auto-fill):
```javascript 
  HTML
    <div id="iframe-container" />

  Javascript
    const email = 'user@email.com';
    const origem = window.location.hostname;
    
    const iframe = document.createElement('iframe');
    iframe.src = `https://app.galaxies.gg/survey/6812a81a0ebb69d258dceaed?sourcePath=${origem}&email=${encodeURIComponent(email)}`;
    iframe.style = "position:absolute;top:0;left:0;width:100%;height:100%;border:0;";
    iframe.setAttribute("allowfullscreen", "");
    iframe.setAttribute("loading", "lazy");
    iframe.setAttribute("sandbox", "allow-scripts allow-same-origin allow-forms");
    
    document.getElementById('iframe-container').appendChild(iframe);

```


