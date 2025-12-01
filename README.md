# 📌 AI Image & Video Generator API

A powerful and user-friendly REST API for generating high-quality **AI Images** and **AI Videos** using text prompts. Designed for developers, automation systems, and production-ready AI applications.

---

## ⚠️ Disclaimer

I’m a student and this project is for educational purposes only.  
Please do **not** use this API for any illegal activity.

## 🚀 Base URL

```
https://mazid-ai.vercel.app/
```

---

## 🔑 Authentication

All requests require an authentication key:

```
api_key = MazidSpace
```

> Requests without a valid API key will be rejected.

---

## 📍 Endpoints

### 1️⃣ Generate Ai Response (ChatBot)

```
GET /GenText
```

#### Required Parameters

| Parameter | Type   | Required | Description                               |
| --------- | ------ | -------- | ----------------------------------------- |
| prompt    | string | Yes      | Your Text query's  |
| api_key   | string | Yes      | Authentication key                        |

#### Example Request

```
https://mazid-ai.vercel.app/GenText?prompt=hello how are you&api_key=MazidSpace
```

#### Response Type

* `json`

#### Example Response
```
{
  "response": "Hey! I'm doing well, thanks for asking. How about you? What's on your mind today?"
}
```
---


### 2️⃣ Generate AI Image

```
GET /GenImage
```

#### Required Parameters

| Parameter | Type   | Required | Description                                  |
| --------- | ------ | -------- | -------------------------------------------- |
| prompt    | string | Yes      | Text description of the image to generate    |
| ratio     | string | Yes      | Output aspect ratio (supported values below) |
| api_key   | string | Yes      | Authentication key                           |

#### Supported Aspect Ratios

```
["1:1", "16:9", "2:3", "3:2", "4:5", "5:4", "9:16", "21:9", "9:21"]
```

#### Example Request

```
https://mazid-ai.vercel.app/GenImage?prompt=beautiful anime girl&ratio=1:1&api_key=MazidSpace
```

#### Response Type

* `image/jpeg`
* `image/png`

---

### 3️⃣ Generate AI Video

```
GET /GenVideo
```

#### Required Parameters

| Parameter | Type   | Required | Description                               |
| --------- | ------ | -------- | ----------------------------------------- |
| prompt    | string | Yes      | Text description of the video to generate |
| api_key   | string | Yes      | Authentication key                        |

#### Example Request

```
https://mazid-ai.vercel.app/GenVideo?prompt=cyberpunk street rainy night&api_key=MazidSpace
```

#### Response Type

* `video/mp4`

---

## ⚠ Error Responses

| Status Code | Meaning                       |
| ----------- | ----------------------------- |
| `200`       | Successful request            |
| `400`       | Missing or invalid parameters |
| `500`       | Internal server error         |

---

## ⭐ Support

If you find this project useful, please consider giving it a ⭐ on GitHub.
