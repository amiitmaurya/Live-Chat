# 💬 Live Chat Application (SignalR)

A real-time chat application built using ASP.NET and SignalR that allows users to communicate instantly without refreshing the page.

---

## 🚀 Features

- Real-time messaging (no page reload)
- Multiple users support
- Broadcast messages to all users
- Fast and responsive UI
- Auto updates using SignalR
- Simple and clean architecture

---

## 🛠️ Tech Stack

- Frontend: HTML, CSS, JavaScript  
- Backend: ASP.NET  
- Real-time Communication: SignalR  
- Database (optional): SQL Server  

---

## 📂 Project Structure

LiveChatApp/
│── Hubs/
│   └── ChatHub.cs
│── wwwroot/
│   ├── css/
│   ├── js/
│   │   └── chat.js
│── Pages/
│   └── Index.cshtml
│── Program.cs
│── appsettings.json
│── README.md

---

## ⚙️ Setup Instructions

1. Clone the repository  
git clone https://github.com/your-username/live-chat-signalr.git

2. Open in Visual Studio  

3. Restore dependencies  
dotnet restore

4. Run the project  
dotnet run

5. Open browser  
https://localhost:xxxx

---

## 🧪 Usage

- Enter your name  
- Type a message  
- Click send  
- Message will appear instantly for all users  

---

## 📌 Example Code (SignalR Hub)

using Microsoft.AspNetCore.SignalR;
using System.Threading.Tasks;

public class ChatHub : Hub
{
    public async Task SendMessage(string user, string message)
    {
        await Clients.All.SendAsync("ReceiveMessage", user, message);
    }
}

---

## 🤝 Contributing

Contributions are welcome!  
Feel free to fork this repo and submit a pull request.

---

## 📄 License

This project is licensed under the MIT License.

---


