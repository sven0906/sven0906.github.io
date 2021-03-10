---
published: true
tags:
  - DRF
  - ViewSet
toc: true
toc_label: ViewSet
categories:
  - Django
---

## ModelViewSet
> .list(), .retrieve(), .create(), .update(), .partial_update(), .destroy()

### 예제
```python
class AccountViewSet(viewsets.ModelViewSet):
    """
    A simple ViewSet for viewing and editing the accounts
    associated with the user.
    """
    serializer_class = AccountSerializer
    permission_classes = [IsAccountAdminOrReadOnly]

    def get_queryset(self):
        return self.request.user.accounts.all()
```


## ReadOnlyModelViewSet

> .list() and .retrieve() 만 허용된다.

### 예제
```python
class AccountViewSet(viewsets.ReadOnlyModelViewSet):
    """
    A simple ViewSet for viewing accounts.
    """
    queryset = Account.objects.all()
    serializer_class = AccountSerializer
```
