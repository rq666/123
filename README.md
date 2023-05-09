# 123
import time
import tkinter as tk

def update_clock():
    now = time.strftime("%H:%M:%S")
    clock_label.config(text=now)
    clock_label.after(1000, update_clock)

# 创建GUI窗口
root = tk.Tk()
root.title("专注时钟")

# 创建显示时间的标签
clock_label = tk.Label(root, font=("Arial", 48), bg="white")
clock_label.pack(padx=20, pady=20)

# 更新时钟
update_clock()

# 运行窗口
root.mainloop()
