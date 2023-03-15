Link thư viện: https://github.com/google/gson 

Phiên bản hiện tại là 2.10.x

### Bước 1: Nhúng vào gradle
```
  implementation 'com.google.code.gson:gson:2.10.1'
```
### Bước 2: Tạo một lớp DTO để tương tác
Tạo lớp java:  User.java
```java
public class User {
    public int id;
    public String name;
}
```
### Bước 3: Trong code activity, tạo đối tượng GSON và đối tượng User để chuyển đổi
```
 //1. Chuyển đối tượng java thành chuỗi JSON
        User objU = new User();
        objU.id = 11;
        objU.name = "Nguyễn Văn A";
        // tạo đối tượng Gson
        Gson gson = new Gson();
        String chuoi_json = gson.toJson(objU );
        Log.d(TAG, "onCreate: Chuỗi json = " + chuoi_json);
```
