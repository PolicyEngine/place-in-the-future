# Who lives near the pilot

Live at https://policyengine.github.io/place-in-the-future/. A dummy module for embedding: household numbers for one place under each alternative on the table. Every number is a placeholder (`MOCK_DATA` in `index.html`), and the page says so in its banner. Places are the three the site's evidence library cites: Loudoun County, Chandler, and Warren County.

Single file, no build step, no dependencies beyond the Inter font. It is iframe-friendly and posts its height to the parent page.

## Embed

```html
<iframe id="place-module" src="https://policyengine.github.io/place-in-the-future/" style="width:100%;border:0" height="1000" title="Who lives near the pilot"></iframe>
<script>
  addEventListener("message", (e) => {
    if (e.data && e.data.type === "place-module-height") document.getElementById("place-module").height = e.data.height;
  });
</script>
```

## What a pilot replaces

Microcosm builds the households of the place, calibrated to published totals. PolicyEngine runs current tax and benefit law over them under each alternative. Axiom encodes the rules the project runs under, cited to their source. The rules list, the bill changes, and the net-income changes are all placeholders until then.

## License

Code in this repository is released under the [MIT License](LICENSE). Original text and figures are released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) with attribution to PolicyEngine. Third-party data and materials keep their own terms.
