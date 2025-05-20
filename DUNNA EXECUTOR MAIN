import tkinter as tk
from tkinter import messagebox
import webbrowser

def rickroll():
    webbrowser.open("https://www.youtube.com/watch?v=xvFZjo5PgG0")

def reset_ui():
    window.configure(bg="#1e1e1e")
    for widget in window.winfo_children():
        widget.destroy()
    setup_gui()

def execute_prank():
    # Clear the GUI
    for widget in window.winfo_children():
        widget.destroy()
    window.configure(bg="white")

    # Show fake "DEVICE HACKED"
    hacked_label = tk.Label(
        window,
        text="DEVICE HACKED",
        fg="red",
        bg="white",
        font=("Segoe UI", 24, "bold")
    )
    hacked_label.pack(expand=True)

    # Wait 2 seconds, then reset and show message
    window.after(2000, lambda: [
        reset_ui(),
        messagebox.showwarning(
            "Malware Disabled...",
            "You're lucky the malware is disabled... but...\nIDK WHAT MONTH FOOLS!"
        )
    ])

def setup_gui():
    # Title
    title = tk.Label(window, text="AWP Executor", fg="white", bg="#1e1e1e", font=("Segoe UI", 18, "bold"))
    title.pack(pady=20)

    # Fake script box
    script_box = tk.Text(
        window, height=6, width=50,
        bg="#2d2d2d", fg="white",
        insertbackground="white",
        borderwidth=0,
        font=("Consolas", 10)
    )
    script_box.pack(pady=5)

    # Button frame
    button_frame = tk.Frame(window, bg="#1e1e1e")
    button_frame.pack(pady=25)

    # Inject button
    inject_btn = tk.Button(
        button_frame,
        text="Inject",
        command=rickroll,
        bg="#2d2d2d",
        fg="white",
        font=("Segoe UI", 11, "bold"),
        activebackground="#444444",
        activeforeground="white",
        bd=0,
        width=15,
        height=2
    )
    inject_btn.grid(row=0, column=0, padx=10)

    # Execute button
    execute_btn = tk.Button(
        button_frame,
        text="Execute",
        command=execute_prank,
        bg="#2d2d2d",
        fg="white",
        font=("Segoe UI", 11, "bold"),
        activebackground="#444444",
        activeforeground="white",
        bd=0,
        width=15,
        height=2
    )
    execute_btn.grid(row=0, column=1, padx=10)

# Initialize window
window = tk.Tk()
window.title("AWP Executor")
window.geometry("450x300")
window.configure(bg="#1e1e1e")
window.resizable(False, False)

setup_gui()
window.mainloop()
