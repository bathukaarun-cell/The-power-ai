function sendMessage(){

const input =
document.getElementById("userInput");

const chat =
document.getElementById("chatBox");

const text = input.value.trim();

if(text==="") return;

chat.innerHTML +=
`<div class="user">${text}</div>`;

let reply =
"The Power AI is thinking...";

if(text.toLowerCase().includes("hello")){
reply = "Hello! Welcome to The Power AI.";
}
else if(text.toLowerCase().includes("who are you")){
reply = "I am The Power AI assistant.";
}
else{
reply =
"Thanks for your message. Connect me to an AI API for real intelligence.";
}

setTimeout(()=>{
chat.innerHTML +=
`<div class="bot">${reply}</div>`;
chat.scrollTop = chat.scrollHeight;
},500);

input.value="";
}
