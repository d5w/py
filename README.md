‏try:  
‏    import requests 
‏    import uuid 
‏    import time 
‏except Exception as e: 
‏    print(e) 
‏logo = ("""
  
          ("--------------------------")
‏          ("Follow me instagram @uti8.rip")
          ("--------------------------")
""")
 
‏print(logo) 
‏user = input('Enter username: ') 
‏password = input('Enter password: ') 
‏target = str(input(("Target:"))) 
‏sle = int(input("Enter sleep: ")) 
‏def login(): 
‏    global target 
‏    r = requests.Session() 
 
‏    uid = str(uuid.uuid4()) 
 
‏    url = "https://i.instagram.com/api/v1/accounts/login/" 
 
‏    headers = { 
‏        'User-Agent': 'Instagram 113.0.0.39.122 Android (24/5.0; 515dpi; 1440x2416; huawei/google; Nexus 6P; angler; angler; en_US)', 
‏        "Accept": "*/*", 
‏        "Accept-Encoding": "gzip, deflate", 
‏        "Accept-Language": "en-US", 
‏        "X-IG-Capabilities": "3brTvw==", 
‏        "X-IG-Connection-Type": "WIFI", 
‏        "Content-Type": "application/x-www-form-urlencoded; charset=UTF-8", 
‏        'Host': 'i.instagram.com' 
    } 
 
‏    data = { 
‏        '_uuid': uid, 
‏        'username': user, 
‏        'enc_password': '#PWD_INSTAGRAM_BROWSER:0:1589682409:{}'.format(password), 
‏        'queryParams': '{}', 
‏        'optIntoOneTap': 'false', 
‏        'device_id': uid, 
‏        'from_reg': 'false', 
‏        '_csrftoken': 'missing', 
‏        'login_attempt_count': '0' 
    } 
 
‏    loginreq = r.post(url, data=data, headers=headers, allow_redirects=True) 
‏    print(lo
