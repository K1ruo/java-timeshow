# java label 标签设置时间
label.setText(new Date().toString());

这是只显示一次，如果要是想要变成动态的，就要加线程事件了。

```
//动态标签时间设置
new Thread(new Runnable() {
              @Override
            public void run() {
                while(true){
         label.setText(new Date().toString());
                    try {
                        Thread.sleep(1000);
                 } catch (InterruptedException e) {
            // TODO Auto-generated catch block
                e.printStackTrace();
             }
             }    
             }
        }).start();
        
