# Discordbotspam
แค่การศึกษาเท่านั้น | Education purpose only

========================================
แค่การศึกษาเท่านั้น | Education purpose only
========================================

local discordia = require('discordia')
local client = discordia.Client()
local prefix = "+" ----- คำนำหน้า

client:on('messageCreate', function(message)
    local content = message.content

    if content:lower():sub(1,#"se") == prefix.. "se" then ----------- se เปลื่อนเป็นอะไรก็ได้
    else
        message:reply{
            embed = {
                title = "เขียนอะไรก็ได้",
                description = "เขียนอะไรก็ได้",
                image = {
                    url = "Link รูปภาพ",
                },
                    footer = {                
                        text = "เขียนอะไรก็ได้",
                        icon_url = "Link รูปภาพ"
                    },
                    fields = {
                }
            }
            
        }
    end
end)

client:run("Bot " ..io.open("./token.txt"):read())     --------- token.txt เป็นไฟเอาไว้ใส่ Token ถ้าคุณไม่มีเเนะนำให้สร้างไปที่ชื่อ token.txt ในไฟเปิดบอท
