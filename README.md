# julia-from-balon-for-maja
https://www.facebook.com/100001227232154/videos/3769357209781816/

Kiedyś bawiłem się fraktalami, więc postanowiłem upchnąć w 16 linijkach fraktal Julii dla Mai. Plus wpłata oczywiście poszła.

Wyjaśnienie akcji: www.code16challenge.pl

Link do zbiórki: www.siepomaga.pl/code16challenge

```html
<html><body><canvas id="canv" width="200" height="200"/><script>
setInterval(()=>{
	for(pixel=0,cx=-2,cy=-2; pixel<40000; pixel++,cx=-2+(pixel/200)/50,cy=-2+(pixel%200)/50) {
		i = 0;
		do {
			xt=cx*cx-cy*cy+(-.8+.6*Math.sin(Date.now()/(3.14*200)));
			cy=2*cx*cy+(.156+.4*Math.cos(Date.now()/(3.14*400)));
			cx=xt;
		} while ((cx*cx+cy*cy<4)&&i++<16);
		(ctx = document.getElementById('canv').getContext('2d')).beginPath();
		ctx.rect(pixel/200, pixel%200, 4, 4);
		ctx.fillStyle = '#'+i+i+i;
		ctx.fill();
	}
},10); 
</script></body></html>
```
