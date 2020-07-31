# zeli

functional programming visualization

# example

```js
// input
zeli(`[rect = {width: '100'}, rect]
    --> group
    --> svg`,
    {
      output: 'json' // [json, mermaid] default object
    }
);

// output
// json
{
  "node": {
    "rect": {
      "takes": []
    },
    "group": {
      "takes": [
        {
          "rect": {
            "width": "100"
          }
        },
        {
          "rect": {}
        }
      ]
    },
    "svg": {
      "takes": [
        {
          "group": {}
        }
      ]
    }
  },
  "endpoint": "svg"
}

// mermaid
# see: https://mermaid-js.github.io/mermaid-live-editor/#/edit/eyJjb2RlIjoiZ3JhcGggVERcbjBWR2RfMGpLS2NrW3JlY3RdIC0tPiAzTGxObXNEYmxia1tncm91cF1cbmlCYTd4UFlJSmstW3JlY3RdIC0tPiAzTGxObXNEYmxia1tncm91cF0gLS0+IEp3U1ZoTUNhTXVQW3N2Z10iLCJtZXJtYWlkIjp7InRoZW1lIjoiZGVmYXVsdCJ9fQ==
graph TD
0VGd_0jKKck[rect] --> 3LlNmsDblbk[group]
iBa7xPYIJk-[rect] --> 3LlNmsDblbk[group] --> JwSVhMCaMuP[svg]
```
