# WiR
### _Work in Reverse_
_WiRwhatWiR
```html
<body>
        <div id="render"></div>
        <div id="viewof-distancex"></div>
         <div id="viewof-distancey"></div>
          <div id="viewof-fontsize"></div>
        </div>
    <script type="module">
        import {Inspector, Runtime} from "https://unpkg.com/@observablehq/notebook-runtime@1.0.1?module";
        import notebook from "https://api.observablehq.com/@kuquanghuylcb/ascii-gradient.js?";
        
        const renders = {
            "render": "#render",
            "viewof distancex": "#viewof-distancex",
            "viewof distancey": "#viewof-distancey",
            "viewof fontsize": "#viewof-fontsize",
            
        };
    
    Runtime.load(notebook, (variable) => {
                 const selector = renders[variable.name];
                 if (selector) {
                 return new Inspector(document.querySelector(selector));
                 }
                 });
        </script>
```
