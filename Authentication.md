# In Django default authentication
| Purpose                                | Import                                                      |
| -------------------------------------- | ----------------------------------------------------------- |
| Authenticate credentials               | `from django.contrib.auth import authenticate`              |
| Log in a user                          | `from django.contrib.auth import login`                     |
| Log out a user                         | `from django.contrib.auth import logout`                    |
| Protect function-based views           | `from django.contrib.auth.decorators import login_required` |
| Protect class-based views              | `from django.contrib.auth.mixins import LoginRequiredMixin` |
| Create a custom authentication backend | `from django.contrib.auth.backends import BaseBackend`      |
| Check permissions                      | `request.user.has_perm()`                                   |
| Check group membership                 | `request.user.groups.filter(...).exists()`                  |
| Check authentication status            | `request.user.is_authenticated`                             |

# In DRF authentication
| Authentication           | Import                                                                                     |
| ------------------------ | ------------------------------------------------------------------------------------------ |
| SessionAuthentication    | `from rest_framework.authentication import SessionAuthentication`                          |
| BasicAuthentication      | `from rest_framework.authentication import BasicAuthentication`                            |
| TokenAuthentication      | `from rest_framework.authentication import TokenAuthentication`                            |
| RemoteUserAuthentication | `from rest_framework.authentication import RemoteUserAuthentication`                       |
| Custom Authentication    | `from rest_framework.authentication import BaseAuthentication`                             |
| JWTAuthentication        | `from rest_framework_simplejwt.authentication import JWTAuthentication`                    |
| OAuth2Authentication     | `from oauth2_provider.contrib.rest_framework import OAuth2Authentication`                  |
| Social Authentication    | No DRF authentication class; provided by packages like `dj-rest-auth` and `django-allauth` |

