<h2>A simple python application for generating a WiFi QR code</h1>

- <strong>Initialize the class by providing QR code values</strong>

<strong>WiFi_QR_Code</strong>(self, error_correction: int = None, box_size: int = None, border: int = None) -> None

    error_correction: the level of error correction in the QR code, the higher the larger the size | ERROR_CORRECT_L
    box_size: the pixel width of each box in the QR code, the higher the larger resolution
    border: the pixel width of the QR code border, improves readability for a camera | cannot be below 4px


- <strong>Encode WiFi credentials into the raw QR code standard</strong>

<strong>.encode_wifi</strong>(self, ssid: str, password: str, encryption: str = None, hidden: str = None) -> str

    ssid: the network SSID
    password: the network password, if applicable
    encryption: the encryption protocol for the network, if applicable | '', 'WPA', 'WPA2'
    hidden: the visibility of the network | 'True', 'False'


- <strong>Generate the WiFi QR code from provided credentials</strong>

<strong>.generate_wifi_qrcode</strong>(self, wifi_metadata: str, file_name: str, file_directory: str = None, fill_color: tuple = None, back_color: tuple = None) -> str
        
    wifi_metadata: raw QR code metadata outputted from the "encode_wifi" function
    file_name: the name of the file to be saved as | does not require any extension
    file_directory: the folder at which to be saved, if applicable | will save in the same folder
    fill_color: the color for the high state of the QR code | ('250', '250', '250')
    back_color: the color for the low state of the QR code | ('0', '0', '0')
