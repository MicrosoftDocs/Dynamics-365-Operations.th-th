---
title: โมดูลการแชทของ Commerce ด้วย Power Virtual Agents
description: บทความนี้อธิบายถึงโมดูลการแชทของ Commerce ด้วย Power Virtual Agents ที่รวม Microsoft Power Virtual Agents กับเว็บไซต์ Dynamics 365 Commerce
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-07
ms.openlocfilehash: 838990cb638479c9c90ba0e38794ecedd55e95b3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691107"
---
# <a name="commerce-chat-with-power-virtual-agents-module"></a>โมดูลการแชทของ Commerce ด้วย Power Virtual Agents

[!include [banner](includes/banner.md)]

บทความนี้อธิบายถึงโมดูลการแชทของ Commerce ด้วย Power Virtual Agents ที่รวม Microsoft Power Virtual Agents กับเว็บไซต์ Dynamics 365 Commerce

คุณลักษณะการแชทของ Commerce ด้วย Power Virtual Agents จะช่วยให้ลูกค้าอีคอมเมิร์ซของ Dynamics 365 สามารถใช้งานความสามารถแชทบอท Power Virtual Agents เพื่อจัดการกับการสอบถามของพวกเขาได้ สำหรับรุ่น Dynamics 365 Commerce 10.0.30 คุณลักษณะนี้สามารถรวมเข้าในเว็บไซต์อีคอมเมิร์ซได้โดยใช้โมดูลการแชทของ Commerce ด้วย Power Virtual Agents ที่เป็นส่วนหนึ่งของไลบรารีโมดูล Commerce

คุณลักษณะการแชทของ Commerce ด้วย Power Virtual Agents ช่วยให้ธุรกิจบรรลุเป้าหมายต่อไปนี้:

- เพิ่มการมีส่วนร่วมของลูกค้าแบบส่วนบุคคลกับผู้บริโภคของพวกเขา และช่วยปรับปรุงเงินวางประกัน
- เพิ่มการบริการลูกค้าโดยการรวมบอทแชทแบบบริการตนเอง
- ปรับปรุงความพึงพอใจของลูกค้าโดยรวม และเพิ่มยอดขาย

> [!NOTE]
> หากต้องการทราบเกี่ยวกับความแตกต่างระหว่างช่องทาง Omni Dynamics 365 สำหรับ Customer Service และโปรแหรมประยุกต์ Power Virtual Agents ดูที่ [ภาพรวมของโมดูลการแชท Commerce](/commerce-chat-modules-overview.md)

## <a name="prerequisites-for-using-power-virtual-agents"></a><a id="prereq"></a>ข้อกำหนดเบื้องต้นสำหรับการใช้ Power Virtual Agents

เมื่อต้องการใช้คุณลักษณะการสนทนาของ Commerce ด้วย Power Virtual Agents คุณต้องสร้างแชทบอท Power Virtual Agents ให้กับเว็บไซต์อีคอมเมิร์ซของคุณก่อน สำหรับคําแนะนํา ดูที่ [การสร้างบอท Power Virtual Agents](/power-virtual-agents/authoring-first-bot)

หลังจากที่คุณตั้งค่าแชทบอทแล้ว คุณต้องคัดลอกค่าของพารามิเตอร์แชทบอท **รหัสบอท** และ **รหัสผู้เช่า** เพื่อตั้งค่าคอนฟิกประสบการณ์การสนทนาของ Commerce หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีคัดลอกค่าเหล่านี้ ดูที่ [ดึงข้อมูลพารามิเตอร์บอท Power Virtual Agents ของคุณ](/power-virtual-agents/publication-connect-bot-to-custom-application#retrieve-your-power-virtual-agents-bot-parameters)

## <a name="configure-your-e-commerce-site"></a>ตั้งค่าคอนฟิกไซต์อีคอมเมิร์ซของคุณ 

วิธีที่แนะนาในการใช้ประสบการณ์การสนทนากับไซต์อีคอมเมิร์ซองคุณคือ เพื่อเพิ่มโมดูลการสนทนาของ Commerce ด้วย Power Virtual Agents ให้กับบางส่วนของหัวข้อที่ใช้ร่วมกัน ซึ่งใช้บนหน้าไซต์ของคุณ

ในการเพิ่มโมดูลการสนทนาไปยังส่วนย่อยของหัวข้อของไซต์ของคุณในปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนเหล่านี้

1. ในโปรแกรมสร้างไซต์ Commerce สำหรับไซต์ของคุณ ไปยัง **ส่วนย่อย**
1. เลือก **ใหม่**
1. ในกล่องโต้ตอบ **เลือกส่วนย่อย** ให้เลือกโมดูล **การสนทนาของ Commerce ด้วย Power Virtual Agents** ป้อนชื่อส่วนย่อย แล้วเลือก **ตกลง**
1. ในมุมมองเค้าร่าง ให้เลือกช่อง **Msdyn365 pva chat connector**
1. ในบานหน้าต่างคุณสมบัติด้านขวา ให้ทำตามขั้นตอนเหล่านี้:

    1. ภายใต้ **พารามิเตอร์บอท** ในฟิลด์ **Bot Framework Webchat Chat CDN URL** ให้ปล่อยค่าเริ่มต้นไว้ (ตัวอย่างเช่น `https://cdn.botframework.com/botframework-webchat/latest/webchat.js`)
    1. ในฟิลด์ **URL การรับรองความถูกต้อง Bot Framework Direct Line** ให้ปล่อยค่าเริ่มต้นไว้ (ตัวอย่างเช่น `https://powerva.microsoft.com/api/botmanagement/v1/directline/directlinetoken`)
    1. ในฟิลด์ **รหัสบอท** ให้ป้อนค่า **รหัสบอท** Power Virtual Agents ซึ่งคุณคัดลอกมาในส่วน [ข้อเบื้องต้นในการใช้ Power Virtual Agents](#prereq)
    1. ในฟิลด์ **รหัสผู้เช่า** ให้ป้อนค่า **รหัสผู้เช่า** ที่คุณคัดลอก

1. เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในส่วน และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่
1. ไปที่ **ส่วนย่อย** และเปิดส่วนย่อยของส่วนหัวของไซต์ของคุณ
1. ในช่อง **คอนเทนเนอร์เริ่มต้น** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มส่วนย่อย**
1. ในกล่องโต้ตอบ **เลือกโมดูล** ให้เลือกส่วนย่อยการแชทที่คุณสร้างไว้ก่อนหน้า แล้วเลือก **ตกลง**
1. เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในส่วน และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่

## <a name="proactive-chat-parameters"></a>พารามิเตอร์การสนทนาอัตโนมัติ

สำหรับรายการพารามิเตอร์การตั้งค่าคอนฟิกการสนทนาเชิงอัตโนมัติทั้งหมด ดูที่ [พารามิเตอร์การสนทนาอัตโนมัติของโมดูลการสนทนา Commerce](chat-proactive-chat-parameters.md)

> [!NOTE]
> ขณะนี้ Power Virtual Agents ยังไม่รองรับการรับรองความถูกต้อง Azure Active Directory B2C (Azure AD B2C) โดยสนับสนุนการเรียกใช้ Retail Cloud Scale Unit แบบไม่ระบุชื่อ (RCSU) เท่านั้นเพื่อเรียกดูความพร้อมใช้งานของผลิตภัณฑ์หรือโต้ตอบกับ API ที่ไม่ระบุชื่ออื่นๆ การเรียกใช้ไปยัง API ที่มีการรับรองความถูกต้องผ่านแชทบอท Power Virtual Agents จะต้องมีการลงชื่อเข้าใช้ของลูกค้าอย่างชัดแจ้ง

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมของคุณลักษณะการสนทนา Commerce](commerce-chat-overview.md)

[โมดูลการสนทนาของ Commerce ด้วย Omnichannel for Customer Service](commerce-chat-module.md)

[พารามิเตอร์การสนทนาอัตโนมัติของโมดูลการสนทนา Commerce](chat-proactive-chat-parameters.md)
