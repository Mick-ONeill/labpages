# Mkdocs container
[Mkdocs](https://www.mkdocs.org/) is a fantastic static website generator. It's like Docusaurus, but just far less hassle.

I followed [this guide](https://medium.com/@edsonalcalamx/running-nethereum-docs-with-docker-5b8a4c25d42f) on how to containerise the site. 

## Gotchas and notes
- While MKDocs is great for very simple things, you do have to use a little bit of extra config for extending it. 
- I used [this guide](https://mkdocs-mermaid2.readthedocs.io/en/latest/) to enable Mermaid diagrams. Because I love Mermaid diagrams, even though I've so far only used one Mermaid diagram. I'll stop saying Mermaid diagrams now. 
- You will need to resort to some HTML if you want to center images. Example below:
```html
<img src=Picture.svg
        alt="Picture"
        width="800"
        height="600"
        style="display: block; margin: 0 auto" />
```