## Chuyển chuỗi json thành đối tượng

```
String chuoi_json = "{\"id\":1, \"name\":\"Dien thoai\", \"price\":12000 }";
        Log.d(TAG, "onCreate: Chuoi json: " + chuoi_json);
        // chuyển chuỗi thành đối tượng

        try {
            JSONObject jsonObject = new JSONObject( chuoi_json );
            Log.d(TAG, "onCreate: ID = " + jsonObject.get("id") );
            Log.d(TAG, "onCreate: Name = " + jsonObject.get("name") );
            Log.d(TAG, "onCreate: Price = " + jsonObject.get("price") );
        } catch (JSONException e) {
            e.printStackTrace();
        }
```
        
        
## Làm việc với mảng json
```
String mang_json = "[{\"id\":1, \"name\":\"Dien thoai\", \"price\":12000 }, {\"id\":2, \"name\":\"May tinh\", \"price\":111111 } ]" ;

        try {
            JSONArray arr = new JSONArray(mang_json);
            for(int i = 0; i<arr.length(); i++){
                JSONObject obj = arr.getJSONObject(i);
                Log.d(TAG, "onCreate: i = " + i + "---name " + obj.get("name"));
                Log.d(TAG, "onCreate: Chuyển obj về chuỗi: " + obj.toString() );
            }

        } catch (JSONException e) {
            e.printStackTrace();
        }
 ```
