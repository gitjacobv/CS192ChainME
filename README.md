# CS192ChainME
ME for Chain of Responsibility

We have created an abstract class AbstractLogger with a level of logging.
Then we have created three types of loggers extending the AbstractLogger.
Each logger checks the level of message to its level and print accordingly
otherwise does not print and pass the message to its next logger.

<see diagram>

1) Edit the AbstractLogger class such that it has a successor.

    Define a varible protected AbstractLogger nextLogger and provide a method
    to set it.

2) Extend the AbstractLogger class such that we have 3 Concrete Classes namely
   ConsoleLogger, ErrorLogger, and FileLogger. Make sure to assign the loggers
   a level when they are constructed. Lastly, override the method write().

   'Standard Console::Logger'
   'Error Console::Logger'
   'File::Logger'

3) In the ChainPatternDemo class, the AbstractLogger getChainOfLoggers does not
   form a chain, edit the code so that it does.

4) Run the ChainPatternDemo and compare with output.

    *Output*

    Standard Console::Logger: This is an information.
    File::Logger: This is an debug level information.
    Standard Console::Logger: This is an debug level information.
    Error Console::Logger: This is an error information.
    File::Logger: This is an error information.
    Standard Console::Logger: This is an error information.
