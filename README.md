# ASCII_bling

# How to install

## Debian ( Ubuntu )
### Dependencies

For coloring text in the console

`sudo apt install locat`


For shuffling output from the terminal

`sudo apt install shuf`


Add to .bashrc this line


`ls ~/.ASCII_bling/art | shuf | head -1 | xargs -I {} cat ~/.ASCII_bling/art/{} | lolcat`


## Mac

### Dependencies

For coloring text in the console

`brew install locat`


For shuffling output from the terminal

`brew install gshuf`


Add to .zsh this line


`ls ~/.ASCII_bling/art | gshuf | head -1 | xargs -I {} cat ~/.ASCII_bling/art/{} | lolcat`



# Download ASCII Art

Create folder for art:

`mkdir -p ~/.ASCII_bling/art`

Put ascii art in different files under the directory:

`cd ~/.ASCII_bling/art`



# Utility Website for ASCII art

## Javascript

Move onto a specific section of the page: https://www.asciiart.eu/computers/apple

Paste in the console this code to download the images in the download folder:

`function blob(text){
 const b =     new Blob([text], {
    type: ‘text/plain’
});
   return  URL.createObjectURL(b);
}
function download(url) {
  const a = document.createElement(‘a’)
  a.href = url
  a.download = url.split(‘/’).pop()
  document.body.appendChild(a)
  a.click()
  document.body.removeChild(a)
}
$(“.border-header.border-top.p-3 pre”).each(function(index){
    const url = blob(this.textContent);
    download(url)
})`