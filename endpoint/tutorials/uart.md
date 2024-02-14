# UART 

---

UART is supported through the standard `SerialPort` class in `System.IO.Ports`

```cs
EPM815.SerialPort.Initialize(EPM815.SerialPort.Uart8);

var serial = new SerialPort(EPM815.SerialPort.Uart8, 115200, Parity.None, 8, StopBits.One);
serial.DataReceived += (a, b) =>
{
    Console.WriteLine("bytes available: " + serial.BytesToRead);
};

serial.Open();
```