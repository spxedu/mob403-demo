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
        
        
