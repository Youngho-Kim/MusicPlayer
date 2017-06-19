# Service


###  Service
```java
MainActivity에서 startService를 하면 onBind가 실행이 된다. = startService(intent);  
  
그러면 public IBinder onBind(Intent intent)// onBind가 생성이 되면서 
  
onServiceConnected로 IBinder를 리턴값으로 보내게 된다.
public void onServiceConnected(ComponentName name, IBinder binder)
  
그럼 onServiceConnected는 인자로 받은 IBinder로 getService를 사용하게 된다.
public MyService getService(){
}
  
  
 public void onServiceDisconnected(ComponentName name)
// 일반적인 상황에서 호출되지 않음.
// onDestroy에서는 호출되지 않는다.
// 서비스가 살아있는지 아닌지 같은 서비스체크는 이곳에서 되지 않는다.
// 서비스가 도중에 끊기거나 연결이 중단되면 호출된다.
       
         
         
// 서비스와 액티비티 간의 의존성이 없음에도 불구하고 액티비티에서  서비스를 띄웠다는 것은
// 서비스에서 결과처리한 값을 가져오거나 서비스의 값을 조회하기 위해 사용한다.
// 그래서 IBinder의 역할은 액티비티가 서비스에 의존성 없이 값을 참조하기 위해서 IBinder라는 인터페이스를 사용.       
```


