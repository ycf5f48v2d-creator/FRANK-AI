async function send() {
  const input = document.getElementById("input");
  const text = input.value;

  const chat = document.getElementById("chat");

  chat.innerHTML += "<p><b>You:</b> " + text + "</p>";

  input.value = "";

  const res = await fetch("YOUR_BACKEND_URL/chat", {
    method: "POST",
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify({ message: text })
  });

  const data = await res.json();

  chat.innerHTML += "<p><b>AI:</b> " + data.reply + "</p>";
}
