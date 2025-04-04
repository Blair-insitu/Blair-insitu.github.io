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
      <div id="pdf-viewer" style="width: 100%; height: 600px;"></div>

      <script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/2.10.377/pdf.min.js"></script>
      <script>
        var url = 'https://raw.githubusercontent.com/Blair-insitu/Blair-insitu.github.io/main/static/AUV2026_industry_pack_v1.pdf';

        // Asynchronously download the PDF
        pdfjsLib.getDocument(url).promise.then(function(pdf) {
          console.log('PDF loaded');
          
          // Fetch the first page
          pdf.getPage(1).then(function(page) {
            console.log('Page loaded');
            
            var scale = 1.5;
            var viewport = page.getViewport({ scale: scale });

            // Prepare canvas using PDF page dimensions
            var canvas = document.createElement('canvas');
            var context = canvas.getContext('2d');
            canvas.width = viewport.width;
            canvas.height = viewport.height;

            // Append the canvas to the container
            document.getElementById('pdf-viewer').appendChild(canvas);

            // Render the page into the canvas context
            var renderContext = {
              canvasContext: context,
              viewport: viewport
            };
            page.render(renderContext);
          });
        }, function(error) {
          console.error('Error loading PDF: ' + error);
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
