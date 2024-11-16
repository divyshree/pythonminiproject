# Import necessary libraries
import qrcode

def generate_qr(data, filename='generated_qr.png'):
    # Create a QR Code instance with basic configuration
    qr = qrcode.QRCode(
        version=1,  # Adjusts the size of the QR code matrix
        error_correction=qrcode.constants.ERROR_CORRECT_L,
        box_size=10,
        border=4,
    )
    
    # Add data to the QR Code
    qr.add_data(data)
    qr.make(fit=True)

    # Generate and save the image
    img = qr.make_image(fill='black', back_color='white')
    img.save(filename)
    print(f"QR Code generated and saved as {filename}")

# Ask user for input data
data_input = input("Enter the text or URL to generate QR code: ")
generate_qr(data_input)
