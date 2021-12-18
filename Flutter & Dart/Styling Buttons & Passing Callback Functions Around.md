Styling Buttons & Passing Callback Functions Around

In the **next lecture**, we'll learn how to pass callback functions around. If the code shown there should not work immediately, you can replace

1.  final Function selectHandler;

_(what we'll write in the next lecture)_

with

1.  final VoidCallback selectHandler;

Important: Only switch to `VoidCallback` instead of `Function`, if the function you're passing around takes NO parameters, arguments (e.g. selectHandler won't receive any arguments, hence we use `VoidCallback`).

Also in the **next lecture**, we'll add a **background color** to our `RaisedButton`.

If you are using the newer `ElevatedButton` instead of the `RaisedButton`, you will need to apply background color differently.

Instead of what we'll write in the next lecture:

1.  RaisedButton(
2.   color: Colors.blue,
3.   child: ...,
4.   onPressed: ...
5.  )

write

1.  ElevatedButton(
2.   style: ButtonStyle(
3.   backgroundColor: MaterialStateProperty.all(Colors.blue),
4.   ),
5.   child: ...,
6.   onPressed: ...,
7.  ),

Again: **You DON'T have to switch** to `ElevatedButton`, you can stick to `RaisedButton` - in which case you'll write exactly the code shown in the lecture.

If you do switch, you can set the styling as shown above, though one of the **advantages** of `ElevatedButton` over `RaisedButton` is that it will actually pick up your **main theme color by default**. So you don't even need to add that custom blue background color - since our main theme uses `Colors.blue` as a `primarySwatch`, the `ElevatedButton` will assume a blue background color out of the box. You would only need to bring your own styling, if you want to deviate from your main theme or style other aspects of the button.

Side-note: If you would add a `textColor: Colors.white` (we'll do that later in the course), you would instead add a `foregroundColor: MaterialStateProperty.all(Colors.white)` for the `ElevatedButton`.