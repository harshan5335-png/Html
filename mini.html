import socket
import subprocess
import platform
import tkinter as tk
from tkinter import ttk, messagebox


def check_device(ip_address):

    if platform.system() == "Windows":
        command = ["ping", "-n", "1", "-w", "500", ip_address]
    else:
        command = ["ping", "-c", "1", "-W", "1", ip_address]

    try:
        result = subprocess.run(
            command,
            stdout=subprocess.DEVNULL,
            stderr=subprocess.DEVNULL
        )

        return result.returncode == 0

    except Exception:
        return False


def find_hostname(ip_address):

    try:
        return socket.gethostbyaddr(ip_address)[0]
    except:
        return "Unknown"


def scan_network():

    network = network_entry.get().strip()

    if network == "":
        messagebox.showwarning(
            "Input Required",
            "Please enter your network address."
        )
        return

    # Clear previous results
    for item in result_table.get_children():
        result_table.delete(item)

    status_label.config(text="Scanning network...")
    root.update()

    found_devices = 0

    # Scan IP addresses from 1 to 254
    for number in range(1, 255):

        ip_address = network + "." + str(number)

        if check_device(ip_address):

            hostname = find_hostname(ip_address)

            result_table.insert(
                "",
                "end",
                values=(
                    ip_address,
                    hostname,
                    "Active"
                )
            )

            found_devices += 1

        root.update()

    status_label.config(
        text="Scan completed - "
        + str(found_devices)
        + " device(s) found."
    )


def clear_results():

    for item in result_table.get_children():
        result_table.delete(item)

    status_label.config(
        text="Results cleared."
    )


# ============================================================
# MAIN WINDOW
# ============================================================

root = tk.Tk()

root.title(
    "IP Address Scanner and Network Device Discovery System"
)

root.geometry("850x550")

root.resizable(False, False)


# Title
title_label = tk.Label(
    root,
    text="IP Address Scanner and Network Device Discovery System",
    font=("Arial", 18, "bold")
)

title_label.pack(pady=20)


# Input frame
input_frame = tk.Frame(root)
input_frame.pack(pady=10)


tk.Label(
    input_frame,
    text="Network Address:",
    font=("Arial", 12)
).grid(
    row=0,
    column=0,
    padx=10
)


network_entry = tk.Entry(
    input_frame,
    width=20,
    font=("Arial", 12)
)

network_entry.grid(
    row=0,
    column=1,
    padx=10
)

network_entry.insert(
    0,
    "192.168.29"
)


# Scan button
scan_button = tk.Button(
    input_frame,
    text="SCAN NETWORK",
    command=scan_network,
    font=("Arial", 11, "bold"),
    width=15
)

scan_button.grid(
    row=0,
    column=2,
    padx=10
)


# Clear button
clear_button = tk.Button(
    input_frame,
    text="CLEAR",
    command=clear_results,
    font=("Arial", 11),
    width=10
)

clear_button.grid(
    row=0,
    column=3,
    padx=5
)


# Result table
columns = (
    "IP Address",
    "Host Name",
    "Status"
)

result_table = ttk.Treeview(
    root,
    columns=columns,
    show="headings",
    height=17
)


result_table.heading(
    "IP Address",
    text="IP Address"
)

result_table.heading(
    "Host Name",
    text="Host Name"
)

result_table.heading(
    "Status",
    text="Status"
)


result_table.column(
    "IP Address",
    width=250
)

result_table.column(
    "Host Name",
    width=350
)

result_table.column(
    "Status",
    width=150
)

result_table.pack(pady=20)


# Status
status_label = tk.Label(
    root,
    text="Enter your network address and click SCAN NETWORK.",
    font=("Arial", 11)
)

status_label.pack(pady=10)


# Start application
root.mainloop()