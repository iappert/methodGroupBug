# methodGroupBug

Rider solution analysis reports an issue with a method group style invocation in case of genereric event handler definition. See file Views/MethodGroupUsing.razor

```
  <MethodGroups>\Views\MethodGroupsUsing.razor:69 Cannot resolve method 'Create(MethodGroups.Views.MethodGroupsUsing, method group)', candidates are:
  Microsoft.AspNetCore.Components.EventCallback<T> Create<T>(object, Microsoft.AspNetCore.Components.EventCallback) (in class EventCallbackFactory)
  Microsoft.AspNetCore.Components.EventCallback<T> Create<T>(object, Microsoft.AspNetCore.Components.EventCallback<T>) (in class EventCallbackFactory)
  Microsoft.AspNetCore.Components.EventCallback<T> Create<T>(object, System.Action) (in class EventCallbackFactory)
  Microsoft.AspNetCore.Components.EventCallback<T> Create<T>(object, System.Action<T>) (in class EventCallbackFactory)
  Microsoft.AspNetCore.Components.EventCallback<T> Create<T>(object, System.Func<System.Threading.Tasks.Task>) (in class EventCallbackFactory)
  Microsoft.AspNetCore.Components.EventCallback<T> Create<T>(object, System.Func<T,System.Threading.Tasks.Task>) (in class EventCallbackFactory)
```

Expected behavior:
No issue
