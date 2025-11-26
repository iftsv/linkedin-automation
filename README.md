# linkedin-automation

### 1. Press Connect button automation (for English UI)
1.1. Simple JS snippet
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
1.2. Create Browser Bookmarklet
```js
javascript:!async function e(){let l=document.querySelectorAll('button[aria-label^="Invite"]');if(l.length>0)for(let i of l)console.log(`${i} is clicked and waiting for 1 sec!`),i.click(),await new Promise(e=>setTimeout(e,1e3))}();
```
1.3. Go to https://www.linkedin.com/mynetwork/grow/ then scroll down the page to get maximum Connect buttons and call your bookmarklet.
