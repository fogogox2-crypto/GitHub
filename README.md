const express = require("express");
const app = express();

// السيرفر الأول (موقع)
app.get("/", (req, res) => {
  res.send("🌐 هذا السيرفر الأول (الموقع)");
});

// السيرفر الثاني (API)
app.get("/api", (req, res) => {
  res.json({
    message: "🤖 هذا السيرفر الثاني (API)",
    status: "working"
  });
});

// تشغيل السيرفر
const listener = app.listen(process.env.PORT || 3000, () => {
  console.log("🚀 Server merged and running!");
});# GitHub
