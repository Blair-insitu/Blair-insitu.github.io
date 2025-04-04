---
title: Industry
date: 2025-03-12
type: landing
sections:
  - block: contact
    content:
      title: Industry
      text: |
        We welcome participation and support from industry. Below is a list of industry packages. If you are interested in being involved or have any questions, please complete this [MS form](https://forms.office.com/Pages/ResponsePage.aspx?id=-XhTSvQpPk2-iWadA62p2LmyOTW14llJg8BmiSB3VBFUREpDVElHNDU5N1daSVdSRUtVTTJONDNaWC4u) and we will be in touch.

      ## Industry Package PDF

      <div id="pdf-container" style="width: 100%; height: 600px;"></div>

      <script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/2.10.377/pdf.min.js"></script>

      <script>
          const url = "/pdfs/AUV2026_industry_pack_v1.pdf"; // Path to your PDF
          const loadingTask = pdfjsLib.getDocument(url);
          loadingTask.promise.then(pdf => {
              pdf.getPage(1).then(page => {
                  const scale = 1.5; // Zoom level
                  const viewport = page.getViewport({ scale: scale });
                  const canvas = document.createElement("canvas");
                  const context = canvas.getContext("2d");
                  canvas.width = viewport.width;
                  canvas.height = viewport.height;
                  document.getElementById("pdf-container").appendChild(canvas);
                  page.render({
                      canvasContext: context,
                      viewport: viewport
                  });
              });
          });
      </script>

    design:
      columns: '1'
      background:
        image: 
          filename: boss-A_light.png
          filters:
            brightness: 0.4
          parallax: false
          position: center
          size: cover
          text_color_light: false
      spacing:
        padding: ['100px', '0', '100px', '0']

  - block: markdown
    design:
      columns: '1'
      background:
        image: 
          filename: sponsors_d.png
          filters:
            brightness: 1
          parallax: false
          position: center
          size: auto
          text_color_light: true
      spacing:
        padding: ['-300px', '0', '-300px', '0']
      css_class:
---
