# Html-Task-2
1 - Can we add form inside another form ?<br>
2- if we have more than one input-submit what happen ?<br>
3- if we dont have input-submit how we can make form submit ?<br>

<hr>

# 1- Can we add form inside another form ? 

No, HTML does not allow nesting form elements directly. If you try to nest one form inside another, it will result in invalid HTML, and the behavior is undefined. Most browsers will not handle this as expected.

<hr>

# 2- if we have more than one input-submit what happen ? 

If a form contains multiple input-submit buttons:

Only the button that is clicked will trigger the submission.
The value of the clicked input-submit will be included in the form's data during submission (if the button has a name attribute).
<code>
&lt;form action="/submit-form" method="post"&gt;
 &lt;input type="text" name="username" placeholder="Enter your username"&gt;
  &lt;input type="submit" name="action" value="Save"&gt;
  <&lt;nput type="submit" name="action" value="Delete"&gt;
form&gt;
<code>
<hr>


# 3- if we dont have input-submit how we can make form submit ?

A. Use a button with type="submit":
The type="submit" on a <button> works like an input-submit

B. Use JavaScript to submit the form:
You can manually submit a form using JavaScript.
<code>
&lt;form id="myForm" action="/submit-form" method="post&gt;
  &lt;input type="text" name="name" placeholder="Enter your name"&gt;
 &lt;button type="button" onclick="submitForm()">Submit</button&gt;
&lt;/form&gt;

<script>
  function submitForm() {
    document.getElementById('myForm').submit();
  }
</script>
</code>
 



