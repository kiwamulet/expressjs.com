<h3 id='app.delete.method'>app.delete(path, callback [, callback ...])</h3>

Routes HTTP DELETE requests to the specified path with the specified callback functions.
For more information, see the [routing guide](/{{ page.lang }}/guide/routing.html).

You can provide multiple callback functions that behave just like middleware, except
these callbacks can invoke `next('route')` to bypass the remaining route
callback(s). You can use this mechanism to impose pre-conditions on a route, then pass control
to subsequent routes if there's no reason to proceed with the current route.

~~~js
app.delete('/', function (req, res) {
  res.send('DELETE request to homepage');
});
~~~
