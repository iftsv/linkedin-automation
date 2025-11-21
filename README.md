# linkedin-automation

### Press Connect button automation
1) Simple JS snippet
```js
(async function click_connect() {
	const connect_buttons = document.querySelectorAll('button[aria-label^="Invite"]');
	if(connect_buttons.length > 0) {
		for (const button of connect_buttons) {
			console.log(`${button} is clicked and waiting for 1 sec!`);
			button.click();
			await new Promise(resolve => setTimeout(resolve, 1000));
		}
	}
})();
```
2) Create Browser Bookmarklet
```js
javascript:!async function e(){let l=document.querySelectorAll('button[aria-label^="Invite"]');if(l.length>0)for(let i of l)console.log(`${i} is clicked and waiting for 1 sec!`),i.click(),await new Promise(e=>setTimeout(e,1e3))}();
```
3) Go to https://www.linkedin.com/mynetwork/grow/ then scroll down the page and call your bookmarklet
