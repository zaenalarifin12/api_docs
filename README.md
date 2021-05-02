# --- REST API PROVISSION ----

## Register 

* **URL**

    {your_host}/api/v1/auth/login

* **Method**

    `POST`

**Request Body**
```
{
    "name"        : "zainal"
    "email"       : "zaenal@gmail.com"
    "password"    : "zaenal123"
}
```

**Response Body**
```
{
    status      : "success"
    data        : {
        "id"          : 1
        "name"        : "zainal"
        "email"       : "zaenal@gmail.com"
        "password"    : "zaenal123"
        "token"       : "eyklsjadsas789678sdasdasdasdasldkjasd"
    }
    
}
```

## Login
* **URL**

    {your_host}/api/v1/auth/login

* **Method**

    `POST`

**Request**
```
{
    email       : zaenal@gmail.com
    password    : zaenal123
}
```

**Response**
```
{
    "status"    :"success",
    "data"      : {
        "id"          : "1",
        "email"       : "zaenal@gmail.com",
        "password"    : "zaenal123",
        "token"       : "5545454dfsdfsdgf54f55y"
    }
    
}
```

## Upload image
* **URL**

    {your_host}/api/v1/upload-image

* **Method**

    `POST`

* **Header**

    `Content-Type: Multipart/form-data`

**Request Body**
```
{
    image           : image.png
}
```

**Response Body**
```
{
    "status"          : "success",
    "data"            : {
        "image"           : "/image/image.png"
    }
}
```

## AllArticle
* **URL**

    {your_host}/api/v1/articles

* **Method**

    `GET`

```
{
    "status"    : "success"
    "data"      : [
        {
            "id"              : 1 
            "slug"            : "Lorem-Ipsum-has-been-the industry's-standard-dummy-text",
            "title"           : "Lorem Ipsum has been the industry's standard dummy text",
            "description"     : "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop p",
            "image"           : "/image/image.png",
            "user"            : {
                "name" : "zaenal",
                "email": "zaenal@gmail.com"
            }
        },
        {
            "id"              : 2
            "slug"            : "Lorem-Ipsum-has-been-the industry's-standard-dummy-text",
            "title"           : "Lorem Ipsum has been the industry's standard dummy text",
            "description"     : "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop p",
            "image"           : "/image/image.png",
            "user"            : {
                "name" : "arifin",
                "email": "arifin@gmail.com"
            }
        },
    ]
}

```


## AddArticle
* **URL**

    {your_host}/api/v1/articles

* **Method**

    `POST`

**Request Body**
```
{
    "title"           : "Lorem Ipsum has been the industry's standard dummy text",
    "description"     : "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop p",
    "image"           : "/image/image.png",
}
```

**Response Body**
```
{
    "status"    : "success",
    "data"      : {
        "id"              : 1
        "slug"            : "Lorem-Ipsum-has-been-the industry's-standard-dummy-text",
        "title"           : "Lorem Ipsum has been the industry's standard dummy text",
        "description"     : "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop p",
        "image"           : "/image/image.png",
    } 
    
}
```

## ShowArticle
* **URL**

    {your_host}/api/v1/articles/1

* **Method**

    `GET`

```
{
    "status": "success"
    "data:  : {
        "id"              : 1 
        "slug"            : "Lorem-Ipsum-has-been-the industry's-standard-dummy-text",
        "title"           : "Lorem Ipsum has been the industry's standard dummy text",
        "description"     : "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop p",
        "image"           : "/image/image.png",
        "user"            : {
            "name" : "zaenal",
            "email": "zaenal@gmail.com"
        },
         "comments"       : [
            {
                id      : 1,
                body    : "komen",
                user    : {
                    name    : arifin,
                    email   :arifin@gmail.com
                }
            }
        ]
    }
},

```


## UpdateArticle
* **URL**

    {your_host}/api/v1/articles/1

* **Method**

    `PUT`

**Request Body**
```
{    
    "title"           : "Lorem Ipsum has been the industry's standard dummy text",
    "description"     : "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop p",
    "image"           : "/image/image.png",
}
```

**Response Body**
```
{    
    "status"            : "success",
    "data"              : {
            "id"                : 2
            "slug"              : "Lorem-Ipsum-has-been-the-industry's-standard-dummy-text",
            "title"             : "Lorem Ipsum has been the industry's standard dummy text",
            "description"       : "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop p",
            "image"             : "/image/image.png",
            "edited"            : true
            "user"              : {
                "name" : zaenal
                "email": zaenal@gmail.com
            }
    }
    
}
```

## DeleteArticle
* **URL**

    {your_host}/api/v1/articles/1

* **Method**

    `DELETE`

```
{    
    "status"          : success,
    "message"         : article has been deleted
}
```

## AddComment
* **URL**

    {your_host}/api/v1/articles/1/comments

* **Method**

    `POST`

**Request Body**
```
{    
    body           : "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also t",
}
```

**Response Body**
```
{    
    "status"    : success,
    "data"      : {
        "id"              : 1
        "body"            : "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also t",
        "user"            : {
            "name" : arifin
            "email": arifin@gmail.com
        }
    }
    
}
```

## updateComment
* **URL**

    {your_host}/api/v1/articles/1/comments/1

* **Method**

    `POST`

**Request**
```
{    
    "body" : "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also t",
}
```

**Response**
```
{    
    "status"    : success,
    "data"      : {
        "id"              : 1
        "body"            : "Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also t",
        "user"            : {
            "name" : arifin
            "email": arifin@gmail.com
        }
    }
    
}
```
## deleteComment

* **URL**

    {your_host}/api/v1/articles/1/comments/1

* **Method**

    `DELETE`

**Response**
```
{    
    "status"  : "success"
    "message" : "comment has been deleted"
}
```

