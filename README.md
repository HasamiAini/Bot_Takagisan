# Bot_Takagisan
Data_Bot_Takagisan

##how to use the data above
## follow the command below

``          
```
`` 
for text based
case '!semangat':
            fetch('https://raw.githubusercontent.com/HasamiAini/Bot_Takagisan/main/motivasi.txt')
            .then(res => res.text())
            .then(body => {
                let splitmotivasi = body.split('\n')
                let randommotivasi = splitmotivasi[Math.floor(Math.random() * splitmotivasi.length)]
                takagisan.reply(from, randommotivasi, id)
            })
            .catch(() => {
                takagisan.reply(from, '*Gomenasai Onichan Ada yang error!*', id)
            })
            break
```
```
`` 
for image based
case '!kpop':
        if (!isGroupMsg) return takagisan.reply(from, 'Gomenasai（>﹏<）Fitur Ini Harus Digroup..!', id)
            if (args.length == 0) return takagisan.reply(from, `Untuk menggunakan ${prefix}kpop\nSilahkan ketik: ${prefix}kpop [query]\nContoh: ${prefix}kpop bts\n\nquery yang tersedia:\nblackpink, exo, bts, twice`, id)
            if (args[0] == 'blackpink' || args[0] == 'exo' || args[0] == 'bts' || args[0] == 'twice') {
                fetch('https://raw.githubusercontent.com/HasamiAini/Bot_Takagisan/main/' + args[0] + '.txt')
                .then(res => res.text())
                .then(body => {
                    let randomkpop = body.split('\n')
                    let randomkpopx = randomkpop[Math.floor(Math.random() * randomkpop.length)]
                    takagisan.sendFileFromUrl(from, randomkpopx, '', '*chwihada*\n*BY:Bot_Takagisan Vers.4.5*\nSupport Bot..*Owner Bot:08319173552*\n*!donasi*', id)
                })
                .catch(() => {
                    takagisan.reply(from, '*Gomenasai Onichan Ada yang error!*', id)
                })
            } else {
                takagisan.reply(from, `Gomenasai Onichan Bukan seperti itu ${prefix}kpop untuk melihat list Perintah`)
            }
            break
```
