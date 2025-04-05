# 🎼 Modusica - Hierarchical Modular Host Framework

> **Modusica** is a fully modular, extensible application host framework built on WPF,  
> designed to **delegate all control to independently developed extensions**—including the UI.  
> Originally a music player, Modusica has evolved into an experimental platform  
> capable of powering highly dynamic and deeply hierarchical application environments.

---

## 🔥 Core Concepts

- **🌲 Fully Hierarchical Structure**  
  Everything—UI, windows, sessions, and even commands—is modeled as a **tree structure**.  
  This allows for powerful nesting, dynamic parenting, and recursive operations like logging, disposing, and bubbling notifications.

- **🎯 Extension-First Design**  
  The host application provides only the core infrastructure.  
  **UI, logic, and behavior are entirely defined by extensions**, allowing for complete control from the outside.

- **🪟 Window & Session Tree**  
  Windows and logical sessions are not flat—they are **nested** and fully managed through a **shared hierarchical interface**, enabling fine-grained control over context, ownership, and lifetime.

- **🧠 Command / Query / Event Messaging**  
  All operations are abstracted as **commands, queries, and events**, with extensible message handling over **NamedPipe** using **MessagePack or JSON** serialization.

- **🧩 Dynamic UI Injection**  
  Extensions can inject UI elements into a shared virtual UI tree, or even provide entire windows.  
  Rendering can be done via XAML, overlays, or streamed visuals.

- **📦 Secure by Design**  
  Extensions must communicate through safe APIs and **cannot directly access internal state**, ensuring sandbox-like modularity.

- **🔁 Undo & History**  
  All commands are tracked and reversible where supported, with undo/redo history per session.

---

## 🚀 Project Status

Modusica is under **active experimental development**.  
Implementation is incremental and uncompromising in design intent.  
The structure may evolve, but every change must serve clarity, modularity, or control.

Current focus areas include:

- Finalizing the hierarchical session/window structure  
- Generalizing command/event systems to support deeply nested contexts  
- UI rendering & editor extensions  
- Strengthening isolation and lifecycle control of extensions  
- Creating tooling for custom extension development

---

## 💡 Who is Modusica for?

- **Framework Creators**  
  Want to build an app where **all logic and UI are modular and replaceable**? Modusica is your foundation.

- **Extension Developers**  
  Build powerful, self-contained extensions that can inject logic, windows, or whole UI layers into the host.

- **Architects & Experimenters**  
  Explore what it means to build a truly dynamic, recursive, and sandboxed environment with a minimal but powerful core.

---

## 🌌 Design Philosophy

- Every UI or logic unit is a **node**. Nodes can have children and parents.  
- All behavior is **context-sensitive** to its session/window hierarchy.  
- Logging, notifications, and resource lifetimes follow the same structure.  
- **There is no default UI**—even `MainWindow` can be defined by an extension.

> Modusica is not just a host.  
> It's a **container for structure**, a **root for logic**, and a **platform for worlds**.

---

## ✳️ Notes on Documentation

This README was partially written with the help of ChatGPT to polish the language and better express the underlying design philosophy.  
All architectural concepts, system design, and structural ideas are original to the author.

---

## 📄 License

This project is not open-source.  
Please contact the author for access or licensing information.

---

## 🧪 Example Use Cases

- **Media player** with layered UI and pluggable playback engines  
- **Toolbox-based editor** where every panel is a detachable, replaceable extension  
- **Interactive data browser** with recursive filtering sessions  
- **Developer shell** with command debugger, extension loader, and live log trees
