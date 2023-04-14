## 项目启动 
npm install

npm run server

## ①  js 中几种常用循环的跳出本次循环和终止循环的方式；
return , break, continue， break + label

## ② 一个循环体中，等待每步循环逻辑执行完毕后，再执行下一步；
function waitStep(i) {
  return new Promise(resolve => {
    setTimeout(() => {
      console.log(`循环的逻辑`); 
      resolve();
    }, 1000); 
  });
}

async function runLoop() {
  for (var i = 0; i < 10; i++) {
    await waitStep(i); 
  }
}

runLoop();

## 弹窗的封装
1 很多成熟的组件库基本都实现了，且功能很全面
2 可以结合组件库进行二次开发



