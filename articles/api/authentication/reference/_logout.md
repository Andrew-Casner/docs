# Logout

This endpoint will logout a user from the identity provider that they logged in with.

```shell
GET https://${account.namespace}/logout?
  returnTo=	  
  &client_id=	{client-id}
```

```ruby
ruby
```

```python
python
```

```csharp
csharp
```

```php
php
```

```java
java
```

<aside class="notice">
For more information, see: <a href="/logout"> Logout</a>.
</aside>

### HTTP Request

`GET https://${account.namespace}/logout?`

### Query Parameters

| Parameter        | Type       | Description |
|:-----------------|:-----------|:------------|
| `returnTo `      | string     | an `Allowed Logout URL` (optional)|
| `client_id`      | string     | the `client_id` of your app (optional) |

### Remarks

* If the `returnTo` parameter is specified, the user will be redirected to that URL after logout.

* If the `client_id` parameter is included, the `returnTo` URL must be listed in the `Allowed Logout URLs` set at the app level (see [Setting Allowed Logout URLs at the App Level](/logout#setting-allowed-logout-urls-at-the-app-level)).

* If the `client_id` parameter is NOT included, the `returnTo` URL must be listed in the `Allowed Logout URLs` set at the account level (see
[Setting Allowed Logout URLs at the Account Level](/logout#setting-allowed-logout-urls-at-the-account-level)).