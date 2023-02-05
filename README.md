
# DRF_Blog_API




## API Reference

#### Register

```http
  POST /api/account/register
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `first_name` | `string` |  |
| `last_name` | `string` |  |
| `username` | `string` |  |
| `password` | `string` |  |

#### Login

```http
  POST /api/account/login
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `username` | `string` |  |
| `password` | `string` |  |

#### Post Blog

```http
  POST /api/home/blog
```
Requires authentication

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `title`      | `string` |  |
| `blog_text`      | `string` |  |
| `main_image`      | `image` |  |

#### Get items

```http
  GET /api/home
```
Doesn't require authentication

```http
  GET /api/home/api/home/?page=${page_number}
```
| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `page_number`      | `int` | **Optional**. page number |

```http
  GET /api/home/api/home/?search=${search_text}
```
| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `search_text`      | `string` | **Optional**. should be contained by blog_title or blog_text |

#### Get items created by particular user

```http
  GET /api/home/blog
```
Requires authentication


```http
  GET /api/home/api/home/blog/?page=${page_number}
```
| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `page_number`      | `int` | **Optional**. page number |

```http
  GET /api/home/api/home/blog/?search=${search_text}
```
| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `search_text`      | `string` | **Optional**. should be contained by blog_title or blog_text |


