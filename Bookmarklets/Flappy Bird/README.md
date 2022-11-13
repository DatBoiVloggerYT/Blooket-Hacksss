removePipes.js

```
javascript:(function()%7BflappyPhaserGame%3D()%3D%3E%7Blet%20e%3DObject.values(document.querySelector(%22%23phaser-bouncy%22))%5B0%5D.stateNode%3Breturn%20e%5BObject.keys(e).filter((e%3D%3Ee.includes(%22reactInternalInstance%22)))%5D.return%7D%2CsetInterval((()%3D%3E%7Btry%7BflappyPhaserGame().stateNode.state.game.scene.children.list.filter((e%3D%3E%22pipe%22%3D%3De.texture%3F.key)).map((e%3D%3E%7Be.scaleY%3D.1%2Ce.y%3D0%7D))%7Dcatch%7B%7D%7D))%3B%7D)()%3B
```

setScore.js

```
javascript:(function()%7BflappyPhaserGame%20%3D%20()%20%3D%3E%20%7B%0A%20%20%20%20let%20a%20%3D%20Object.values(document.querySelector(%22%23phaser-bouncy%22))%5B0%5D.stateNode%0A%20%20%20%20return%20a%5BObject.keys(a).filter(b%20%3D%3E%20b.includes(%22reactInternalInstance%22))%5D.return%0A%7D%0A%0A(()%20%3D%3E%20%7B%0A%20%20%20%20let%20n%20%3D%20document.createElement('iframe')%3B%0A%20%20%20%20document.body.append(n)%3B%0A%20%20%20%20window.prompt%20%3D%20n.contentWindow.prompt.bind(window)%3B%0A%20%20%20%20n.remove()%3B%0A%7D)()%3B%0A%0AflappyPhaserGame().stateNode.setState(%7B%20score%3A%20parseInt(prompt(%22How%20much%20score%20would%20you%20like%3F%22))%20%7D)%3B%7D)()%3B
```
