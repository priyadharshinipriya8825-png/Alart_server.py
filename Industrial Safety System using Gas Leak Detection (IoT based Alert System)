from flask import Flask, request
import smtplib

app = Flask(__name__)

@app.route('/alert', methods=['POST'])
def alert():
    msg = "Industrial Safety Alert! Gas Leak Detected."
    server = smtplib.SMTP('smtp.gmail.com', 587)
    server.starttls()
    server.login("youremail@gmail.com", "password")
    server.sendmail("youremail@gmail.com", "receiver@gmail.com", msg)
    server.quit()
    return "Alert Sent", 200

if __name__ == "__main__":
    app.run(host="0.0.0.0", port=6000)
