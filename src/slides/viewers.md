# Viewers

- Chrome
- Firefox
- Edge
- ...

,
                    { src: 'lib/plugin/notes/notes.js', async: true },
                    { src: 'lib/plugin/highlight/highlight.js', async: true, callback: function() { hljs.initHighlightingOnLoad(); } }