``` javascript
var user = new Parse.User();
user.set("username", "hackerschool");
user.set("password", "password");
user.set("email", "max@max.max")
user.signUp()
```

``` javascript
<script src="//fb.me/react-0.12.2.min.js"></script>
<script src="//fb.me/JSXTransformer-0.12.2.js"></script>

<script type="text/jsx">
    $(function() {
        if (Parse.User.current()) {
            $('.container').prepend("A user is logged in. The users email is " + Parse.User.current().attributes.email)            
        } else {
            $('.container').prepend("No one is logged in")
        }
    })
    var LoginForm = React.createClass({
        handleSubmit: function(e) {
            e.preventDefault();
            var username = this.refs.username.getDOMNode().value.trim();
            var password = this.refs.password.getDOMNode().value.trim();
            if (!username || !password) {
                return;
            }
            Parse.User.logIn(username, password, {
                success: function(user) {
                    React.render(
                        <div>
                            Username is {user.attributes.username} and 
                            email is {user.attributes.email}
                        </div>,
                        document.getElementById('info')
                    );
                },
                error: function(user, error) {
                    // The login failed. Check error to see why.
                }
            });
            return;
        },
        render: function() {
            return (
                <div>
                    <br />
                    <h3>Romulus</h3>
                    <form className="LoginForm" onSubmit={this.handleSubmit}>
                        <input type="text" placeholder="username" ref="username" />
                        <br />
                        <input type="password" placeholder="password" ref="password" />
                        <br />
                        <input type="submit" value="Login" />
                    </form>
                </div>
            );
        }
    });
    React.render(
        <LoginForm username="maxmcd" />,
        document.getElementById('login')
    ); 
</script>
<div class="container">
    <div id="login"></div>
    <div id="info"></div>
</div>
```