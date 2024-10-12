Issue 1- Background color functionality

Code:- 

let selectedColor = '';
 function changeShapeColor(){
    let divs = document.querySelectorAll('.content div');
    divs.forEach(div => {
      div.style.backgroundColor = selectedColor;
    })
  }

By adding above code we can implement the background color change fuctionality.


Issue 2- Print Functionality

Code:- 

   function downloadAsImage() {
    const element = document.getElementById('content-to-download');

    const paragraphs = element.querySelectorAll('p');
    paragraphs.forEach(p => {
      p.style.display = 'none';
    });

    html2canvas(element).then(canvas => {
      paragraphs.forEach(p => {
        p.style.display = '';
      });

      const url = canvas.toDataURL('image/png');
      const a = document.createElement('a');
      a.href = url;
      a.download = 'download.png';
      a.click();
    });
  }

Above code downloads the entire flowchart into .png format.
It excludes the marquee line which is at the top of the div and rest entire flowchart gets downloaded.

Issue 3- (Additional)

UI Improvement
Home Page Navigation
Logo Visibility