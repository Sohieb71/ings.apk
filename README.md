<!DOCTYPE html>
<html>
<head>
    <title>RC Input for WebSocket</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/crypto-js/4.0.0/crypto-js.min.js"></script>
    <style>
        body {
            font-family: sans-serif;
            background-color: #f4f4f4;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
        }

        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        .socket-container {
            border: 1px solid #ddd;
            padding: 10px;
            margin-bottom: 10px;
            width: 300px;
        }

        .rc {
            width: 160px;
            padding: 8px;
            margin-bottom: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            box-sizing: border-box;
            text-align: center;
        }

        button {
            padding: 8px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            background-color: #007bff;
            color: white;
            margin: 5px;
        }

        .disconnect-btn {
            background-color: #dc3545;
        }

        .nameDisplay,
        .planetDisplay {
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Project By LuCiFeR</h2>
        <div class="socket-container" id="socket1">
            <input type="text" class="rc" placeholder="Recovery Code 1" maxlength="10">
            <select class="devtype">
                <option value="352">Web</option>
                <option value="312">Android</option>
                <option value="323">iOS</option>
            </select>
            <div>
                <button class="connect">Connect 1</button>
                <button class="disconnect disconnect-btn">Disconnect 1</button>
            </div>
            <select class="ringtoss">
                <option value="RingToss*1">RingToss*1</option>
                <option value="RingToss*2">RingToss*2</option>
                <option value="RingToss*3">RingToss*3</option>
                <option value="RingToss*4">RingToss*4</option>
                <option value="RingToss*5">RingToss*5</option>
                <option value="RingToss*6">RingToss*6</option>
                <option value="RingToss*7">RingToss*7</option>
                <option value="RingToss*8">RingToss*8</option>
                <option value="RingToss*9">RingToss*9</option>
                <option value="RingToss*10">RingToss*10</option>
                <option value="RingToss*11">RingToss*11</option>
                <option value="RingToss*12">RingToss*12</option>
                <option value="RingToss*13">RingToss*13</option>
                <option value="RingToss*14">RingToss*14</option>
                <option value="RingToss*15">RingToss*15</option>
                <option value="RingToss*16">RingToss*16</option>
                <option value="RingToss*17">RingToss*17</option>
                <option value="RingToss*18">RingToss*18</option>
                <option value="RingToss*19">RingToss*19</option>
                <option value="RingToss*20">RingToss*20</option>
            </select>
            <button class="fly">Fly 1</button>
            <div class="nameDisplay">Name: </div>
            <div class="planetDisplay">Planet: </div>
        </div>

        <div class="socket-container" id="socket2">
            <input type="text" class="rc" placeholder="Recovery Code 2" maxlength="10">
            <select class="devtype">
                <option value="352">Web</option>
                <option value="312">Android</option>
                <option value="323">iOS</option>
            </select>
            <div>
                <button class="connect">Connect 2</button>
                <button class="disconnect disconnect-btn">Disconnect 2</button>
            </div>
            <select class="ringtoss">
                <option value="RingToss*1">RingToss*1</option>
                <option value="RingToss*2">RingToss*2</option>
                <option value="RingToss*3">RingToss*3</option>
                <option value="RingToss*4">RingToss*4</option>
                <option value="RingToss*5">RingToss*5</option>
                <option value="RingToss*6">RingToss*6</option>
                <option value="RingToss*7">RingToss*7</option>
                <option value="RingToss*8">RingToss*8</option>
                <option value="RingToss*9">RingToss*9</option>
                <option value="RingToss*10">RingToss*10</option>
                <option value="RingToss*11">RingToss*11</option>
                <option value="RingToss*12">RingToss*12</option>
                <option value="RingToss*13">RingToss*13</option>
                <option value="RingToss*14">RingToss*14</option>
                <option value="RingToss*15">RingToss*15</option>
                <option value="RingToss*16">RingToss*16</option>
                <option value="RingToss*17">RingToss*17</option>
                <option value="RingToss*18">RingToss*18</option>
                <option value="RingToss*19">RingToss*19</option>
                <option value="RingToss*20">RingToss*20</option>
            </select>
            <button class="fly">Fly 2</button>
            <div class="nameDisplay">Name: </div>
            <div class="planetDisplay">Planet: </div>
        </div>
        <div class="socket-container" id="socket3">
            <input type="text" class="rc" placeholder="Recovery Code 3" maxlength="10">
            <select class="devtype">
                <option value="352">Web</option>
                <option value="312">Android</option>
                <option value="323">iOS</option>
            </select>
            <div>
                <button class="connect">Connect 3</button>
                <button class="disconnect disconnect-btn">Disconnect 3</button>
            </div>
            <select class="ringtoss">
                <option value="RingToss*1">RingToss*1</option>
                <option value="RingToss*2">RingToss*2</option>
                <option value="RingToss*3">RingToss*3</option>
                <option value="RingToss*4">RingToss*4</option>
                <option value="RingToss*5">RingToss*5</option>
                <option value="RingToss*6">RingToss*6</option>
                <option value="RingToss*7">RingToss*7</option>
                <option value="RingToss*8">RingToss*8</option>
                <option value="RingToss*9">RingToss*9</option>
                <option value="RingToss*10">RingToss*10</option>
                <option value="RingToss*11">RingToss*11</option>
                <option value="RingToss*12">RingToss*12</option>
                <option value="RingToss*13">RingToss*13</option>
                <option value="RingToss*14">RingToss*14</option>
                <option value="RingToss*15">RingToss*15</option>
                <option value="RingToss*16">RingToss*16</option>
                <option value="RingToss*17">RingToss*17</option>
                <option value="RingToss*18">RingToss*18</option>
                <option value="RingToss*19">RingToss*19</option>
                <option value="RingToss*20">RingToss*20</option>
            </select>
            <button class="fly">Fly 3</button>
            <div class="nameDisplay">Name: </div>
            <div class="planetDisplay">Planet: </div>
        </div>
    </div>
    <script>
       const socketData = [];

document.querySelectorAll('.socket-container').forEach((socketContainer, index) => {
    const rcInput = socketContainer.querySelector('.rc');
    const devtypeSelect = socketContainer.querySelector('.devtype');
    const connectButton = socketContainer.querySelector('.connect');
    const disconnectButton = socketContainer.querySelector('.disconnect');
    const ringtossSelect = socketContainer.querySelector('.ringtoss');
    const flyButton = socketContainer.querySelector('.fly');
    const nameDisplay = socketContainer.querySelector('.nameDisplay');
    const planetDisplay = socketContainer.querySelector('.planetDisplay');
    const socketId = index + 1;

    const socketInfo = {
        ws: null,
        haaapsi: null,
        id: null,
        useridg: null,
        passwordg: null,
        nameDisplay: nameDisplay,
        planetDisplay: planetDisplay,
    };
    socketData.push(socketInfo);

    connectButton.addEventListener('click', () => {
        const rc = rcInput.value;
        const devtype = devtypeSelect.value;
        socketInfo.ws = new WebSocket('wss://cs.mobstudio.ru:6672');

        socketInfo.ws.onopen = () => {
            socketInfo.ws.send(`:en IDENT ${devtype} -2 4030 1 2 :GALA\r\n`);

            let planetid = null;
            let waitForGoFlag = false;
            let actionToSend = null;

            socketInfo.ws.onmessage = (event) => {
                const text = event.data;
                const snippets = text.split(';').join(' ').split(' ');
                const message = event.data;

                if (snippets[0] === 'HAAAPSI') {
                    socketInfo.haaapsi = snippets[1];
                    socketInfo.ws.send('RECOVER ' + rc + '\r\n');
                }

                if (snippets[0] === 'REGISTER') {
                    const temp = parseHaaapsi(socketInfo.haaapsi);
                    socketInfo.id = snippets[1];
                    socketInfo.passwordg = snippets[2];
                    socketInfo.useridg = snippets[1];
                    const finalusername = snippets[3].split('\r\n')[0];
                    socketInfo.ws.send(`USER ${socketInfo.id} ${socketInfo.passwordg} ${finalusername} ${temp}\r\n`);
                    socketInfo.nameDisplay.textContent = `Name: ${snippets[3]}`;
                }

                if (snippets[0] === '999') {
                    const phoneMessages = [
                        'PHONE 1366 768 0 2 :chrome 114.0.5735.106',
                        'PHONE 2208 1242 0 2 :firefox 94.0',
                        'PHONE 1536 864 0 2 :opr 80.0.4170.63',
                        'PHONE 1536 864 0 2 :chrome 109.0.5414.75',
                        'PHONE 1536 864 0 2 :chrome 108.0.5359.95',
                        'PHONE 1536 864 0 2 :opr 90.0.4480.84',
                        'PHONE 1536 864 0 2 :opr 85.0.4341.60',
                        'PHONE 1536 864 0 2 :opr 100.0.0.0',
                        'PHONE 1536 864 0 2 :chrome 112.0.5615.138',
                        'PHONE 1536 864 0 2 :chrome 111.0.5563.111',
                        'PHONE 1536 864 0 2 :chrome 113.0.5672.127',
                        'PHONE 2208 1242 0 2 :firefox 98.0',
                        'PHONE 2208 1242 0 2 :firefox 114.0',
                    ];
                    const randomPhoneMessage = phoneMessages[Math.floor(Math.random() * phoneMessages.length)];
                    socketInfo.ws.send('FWLISTVER 281\r\n');
                    socketInfo.ws.send('ADDONS 251055 2\r\n');
                    socketInfo.ws.send('MYADDONS 251055 2\r\n');
                    socketInfo.ws.send(randomPhoneMessage + '\r\n');
                    socketInfo.ws.send('JOIN\r\n');
                }

                if (snippets[0] === 'PING\r\n') {
                    socketInfo.ws.send('PONG\r\n');
                }

                if (message.startsWith('REMOVE_VIEW')) {
                    planetid = message.split(' ')[2];
                } else if (message.startsWith('ADD_VIEW')) {
                    if (message.includes('rt/br-s;40;28;33 10')) {
                        waitForGoFlag = true;
                        actionToSend = `ACTION 10413 ${planetid}\r\n`;
                    } else if (message.includes('rt/br-s;0;28;33 10') || message.includes('rt/sr-s;0;28;33 10')) {
                        waitForGoFlag = true;
                        actionToSend = `ACTION 10414 ${planetid}\r\n`;
                    } else if (message.includes('rt/sr-s;-40;28;33 10') || message.includes('rt/gr-s;-40;28;33 10')) {
                        waitForGoFlag = true;
                        actionToSend = `ACTION 10415 ${planetid}\r\n`;
                    } else if (message.includes('rt/go-flag') && waitForGoFlag) {
                        socketInfo.ws.send(actionToSend);
                        waitForGoFlag = false;
                        actionToSend = null;
                    }
                }

                if(message.startsWith('REGISTER')){
                    if(snippets[3]){
                        socketInfo.nameDisplay.textContent = `Name: ${snippets[3]}`;
                    }
                }

                if(snippets[0] === '353'){
                    if(snippets[3]){
                        socketInfo.planetDisplay.textContent = `Planet: ${snippets[3]}`;
                    }
                }
            };
        };
    });
    disconnectButton.addEventListener('click', () => {
        if (socketInfo.ws) {
            socketInfo.ws.send('QUIT :ds\r\n');
            socketInfo.ws.onclose = () => {
                socketInfo.nameDisplay.textContent = "Name: ";
                socketInfo.planetDisplay.textContent = "Planet: ";
            };
            socketInfo.ws.close();
        }
    });

    flyButton.addEventListener('click', () => {
        const selectedring = ringtossSelect.value;
        if (socketInfo.ws) {
            socketInfo.ws.send(`JOIN ${selectedring}\r\n`);
        }
    });
});

const parseHaaapsi = (e) => {
    var temp = CryptoJS.MD5(e).toString(CryptoJS.enc.Hex);
    return (temp = temp.split('').reverse().join('0')).substr(5, 10);
};
    </script>
</body>
</html>
