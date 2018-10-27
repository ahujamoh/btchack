data = "BCHForEveryone"
 
//'BCHForEveryone'

buf = BITBOX.Script.nullData.output.encode(Buffer.from(data, 'ascii'));
//<Buffer 6a 0e 42 43 48 46 6f 72 45 76 65 72 79 6f 6e 65>
BITBOX.Script.nullData.output.decode(buf).toString('ascii');
//'BCHForEveryone'
BITBOX.Script.nullData.output.decode(buf).toString('ascii') === data
//true
data = "BCHForEveryOne"
//'BCHForEveryOne'
BITBOX.Script.nullData.output.decode(buf).toString('ascii') === data
//false