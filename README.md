import qrcode
import png
qr = qrcode.QRCode(
    version=1,
    error_correction=qrcode.constants.ERROR_CORRECT_L,
    box_size=10,
    border=4,
)
qr.add_data("QR code Generation By Sai Kalyan")
qr.make(fit=True)
img = qr.make_image(fill_color="Black", back_color="white")
img.save("medium.png")
