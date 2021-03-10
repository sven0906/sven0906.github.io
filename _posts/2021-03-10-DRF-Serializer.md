---
published: true
title: "Serializer(시리얼라이저)"
categories:
  - Django
tags:
  - Serializer, REST FRAMEWORK, DRF
---

## Serializing objects

> 복잡한 데이터를 쿼리셋 및 모델 인스턴스로 쉽게 변환시키는 것

We can now use CommentSerializer to serialize a comment, or list of comments. Again, using the Serializer class looks a lot like using a Form class.

```python
serializer = CommentSerializer(comment)
serializer.data
```

## Deserializing objects

Deserialization is similar. First we parse a stream into Python native datatypes...

```python
import io
from rest_framework.parsers import JSONParser

stream = io.BytesIO(json)
data = JSONParser().parse(stream)
```
...then we restore those native datatypes into a dictionary of validated data.

```python
serializer = CommentSerializer(data=data)
serializer.is_valid()
# True
serializer.validated_data
# {'content': 'foo bar', 'email': 'leila@example.com', 'created': datetime.datetime(2012, 08, 22, 16, 20, 09, 822243)}
```

참고 : [DJANGO REST FRAMEWORK 공식 문서](https://www.django-rest-framework.org/api-guide/serializers/#serializers)

