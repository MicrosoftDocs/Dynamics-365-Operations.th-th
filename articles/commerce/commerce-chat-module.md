---
title: โมดูลการสนทนาของ Commerce ด้วย Omnichannel for Customer Service
description: บทความนี้จะอธิบายโมดูลการสนทนาของ Commerce ด้วย Omnichannel for Customer Service ใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: b8eaed3eb015e96b1db6fa2297c341ea9d3ff8ad
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473821"
---
# <a name="commerce-chat-with-omnichannel-for-customer-service-module"></a>โมดูลการสนทนาของ Commerce ด้วย Omnichannel for Customer Service

[!include [banner](includes/banner.md)]

บทความนี้จะอธิบายโมดูล *การสนทนาของ Commerce ด้วย Omnichannel for Customer Service* ใน Microsoft Dynamics 365 Commerce

ใน Commerce เวอร์ชัน 10.0.29 ได้มีการเพิ่มโมดูลการสนทนาของ Commerce ด้วย Omnichannel for Customer Service ใหม่ ลงในไลบรารีโมดูล Commerce คุณลักษณะการสนทนาของ Commerce ให้ความสามารถการสนทนาของ Dynamics 365 Omnichannel for Customer Service แก่ลูกค้าอีคอมเมิร์ซ ซึ่งรวมถึงการสนับสนุนของตัวแทนสดเพื่อช่วยในการสอบถามของลูกค้า ในการบริการลูกค้า และช่วยเหลือการขายของลูกค้า Commerce

คุณลักษณะการสนทนาของ Commerce ช่วยให้ผู้ค้าปลีกสามารถบรรลุเป้าหมายเหล่านี้ได้:

- เพิ่มการมีส่วนร่วมของลูกค้าแบบส่วนบุคคล เพื่อช่วยปรับปรุงเงินวางประกันของลูกค้า
- ปรับปรุงการบริการลูกค้าโดยการรวมเจ้าหน้าที่ฝ่ายทรัพยากรบุคคลและบอทแชทแบบบริการตนเอง
- ช่วยตัวแทนให้ได้รับประสบการณ์ผ่านโพรไฟล์ลูกค้า ใบสั่ง และข้อมูลการซื้อแบบเรียลไทม์ ที่ผลักดันการปรับปรุงการปฏิบัติการและการสนับสนุน
- ปรับปรุงความพึงพอใจของลูกค้าโดยรวม เพื่อช่วยเพิ่มยอดขาย

ความสามารถต่อไปนี้พร้อมใช้งานเป็นส่วนหนึ่งของคุณลักษณะการสนทนาของ Commerce:

- การสนทนาของ Commerce ด้วย Omnichannel for Customer Service
- การเพิ่ม **Commerce Call Center** เป็นแท็บแอปลิเคชันในประสบการณ์ของตัวแทนใน Dynamics 365 Dynamics 365 Dynamicnel for Customer Service

## <a name="prerequisites-for-omnichannel-for-customer-service"></a>ข้อกำหนดเบื้องต้นสำหรับ Omnichannel for Customer Service

ตามข้อกําหนดเบื้องต้น คุณต้องตั้งค่าคอนฟิกการสนทนาในวิดเจ็ต Omnichannel for Customer Service Administration และขอรับพารามิเตอร์บางตัว เพื่อตั้งค่าคอนฟิกประสบการณ์การสนทนาของ Commerce สำหรับคำแนะนำ ดู [ตั้งค่าคอนฟิกช่องทางของแชท](/dynamics365/customer-service/set-up-chat-widget)

หลังจากที่คุณตั้งค่าคอนฟิกการแชทในวิดเจ็ต Omnichannel for Customer Service Administration แล้ว คุณจะได้รับสคริปต์ที่มีลักษณะคล้ายกับตัวอย่างต่อไปนี้

`<script id="Microsoft_Omnichannel_LCWidget" src="https://oc-cdn-ocprod.azureedge.net/livechatwidget/scripts/LiveChatBootstrapper.js" data-app-id="xxxx-xxx-4be7-bcd5-1d118ecffe1f" data-org-id="5a0e73c0-xxxx-xxxxx-xxx- 76df135f375d" data-org-url="https://xxsxxxxssdb348f-crm.omnichannelengagementhub.com"></script>`

คัดลอกสคริปต์นี้ เนื่องจากคุณจะต้องมีค่าในสคริปต์เพื่อตั้งค่าคอนฟิกโมดูลการแชท

### <a name="commerce-chat-with-omnichannel-for-customer-service-mandatory-fields"></a>ฟิลด์บังคับการสนทนาของ Commerce ด้วย Omnichannel for Customer Service

ตารางต่อไปนี้แสดงค่าสคริปต์จากวิดเจ็ต Omnichannel for Customer Service Administration ที่ต้องใช้ในการตั้งค่าคอนฟิกโมดูลการสนทนาของ Commerce ด้วย Omnichannel for Customer Service

| คุณสมบัติของวิดเจ็ต | คำอธิบาย |
| ------------- |--------------|
| แหล่งที่มาของสคริปต์ | ค่าของ **src** ในสคริปต์วิดเจ็ตของแชท |
| รหัสแอปพลิเคชันข้อมูล | ค่าของ **data-app-id** ในสคริปต์วิดเจ็ตของแชท |
| รหัสองค์กรข้อมูล | ค่าของ **data-org-id** ในสคริปต์วิดเจ็ตของแชท |
| URL องค์กรข้อมูล | ค่าของ **data-org-url** ในสคริปต์วิดเจ็ตของแชท |

## <a name="configure-the-commerce-chat-experience-for-your-e-commerce-site"></a>ตั้งค่าคอนฟิกประสบการณ์การสนทนาของ Commerce สำหรับไซต์อีคอมเมิร์ซของคุณ

วิธีที่แนะนาในการใช้ประสบการณ์การสนทนากับไซต์อีคอมเมิร์ซองคุณคือ เพื่อเพิ่มโมดูลการสนทนาของ Commerce ด้วย Omnichannel for Customer Service ให้กับบางส่วนของหัวข้อที่ใช้ร่วมกัน ซึ่งใช้บนหน้าไซต์อีคอมเมิร์ซของคุณ

ในการเพิ่มโมดูลการสนทนาไปยังส่วนย่อยของหัวข้อของไซต์ของคุณในปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนเหล่านี้

1. ในโปรแกรมสร้างไซต์สำหรับไซต์ของคุณ ไปยัง **ส่วนย่อย**
1. เลือก **ใหม่**
1. ในกล่องโต้ตอบ **เลือกส่วนย่อย** ให้เลือกโมดูล **การสนทนาของ Commerce ด้วย Omnichannel for Customer Service** ป้อนชื่อส่วนย่อย แล้วเลือก **ตกลง**
1. ในมุมมองเค้าร่าง ให้เลือกช่อง **Msdyn365 cs chat connector**
1. ในบานหน้าต่าง **คุณสมบัติการแชท** ด้านขวา ให้ทำตามขั้นตอนเหล่านี้:

    1. ในฟิลด์ **แหล่งที่มาของสคริปต์** ให้ป้อนค่า **src** ที่คุณได้รับจากสคริปต์ Omnichannel for Customer Service
    1. ในฟิลด์ **รหัสแอปพลิเคชันของข้อมูล** ให้ป้อนค่า **data-app-id** ที่คุณได้รับจากสคริปต์ Omnichannel for Customer Service
    1. ในฟิลด์ **รหัสองค์กรของข้อมูล** ให้ป้อนค่า **data-org-id** ที่คุณได้รับจากสคริปต์ Omnichannel for Customer Service
    1. ในฟิลด์ **URL องค์กรของข้อมูล** ให้ป้อนค่า **data-org-url** ที่คุณได้รับจากสคริปต์ Omnichannel for Customer Service

    ![การสร้างส่วนย่อยของโมดูลการสนทนาของ Commerce ในโปรแกรมสร้างไซต์ Commerce](media/Commerce-chat-creating-new-fragment.png)

1. เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในส่วน และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่
1. ไปที่ **ส่วนย่อย** และเปิดส่วนย่อยของส่วนหัวของไซต์ของคุณ
1. ในช่อง **คอนเทนเนอร์เริ่มต้น** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มส่วนย่อย**
1. ในกล่องโต้ตอบ **เลือกโมดูล** ให้เลือกส่วนย่อยการแชทที่คุณสร้างไว้ก่อนหน้า แล้วเลือก **ตกลง**
1. เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในส่วน และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่

## <a name="add-commerce-headquarters-as-an-application-tab-for-omnichannel-for-customer-service"></a>เพิ่ม Commerce Headquarters เป็นแท็บแอพลิเคชัน สำหรับ Omnichannel for Customer Service

คุณสามารถเพิ่มแท็บแอพลิเคชันสำหรับ Commerce headquarters ใน Omnichannel for Customer Service จากนั้นตัวแทนสนทนาสดจะสามารถใช้อินเทอร์เฟสผู้ใช้สำหรับประสบการณ์ตัวแทน Omnichannel for Customer Service เพื่อเข้าถึงโมดูล Dynamics 365 Commerce Customer Service ที่มีข้อมูลบริบทของลูกค้าพร้อมกับข้อมูลใบสั่งขายได้โดยง่าย นอกจากนี้ เจ้าหน้าที่บริการลูกค้ายังสามารถวางใบสั่งใหม่ เริ่มต้นการส่งคืน และตรวจสอบความถูกต้องของข้อมูลสถานะของใบสั่งได้

### <a name="create-a-new-application-tab-that-loads-commerce-headquarters-in-an-iframe-module"></a>สร้างแท็บแอปลิเคชันใหม่ ที่โหลด Commerce headquarters ในโมดูล iFrame 

ในการสร้างแท็บแอปลิเคชันใหม่ ที่โหลด Commerce headquarters ในโมดูล iFrame ให้ทำตามขั้นตอนเหล่านี้

1. เปิด [Power Apps Maker Portal](https://make.powerapps.com)
1. ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **Apps**
1. เลือก **ศูนย์การจัดการ Customer Service**
1. ไปที่ **ประสบการณ์ของตัวแทน**
1. ที่ **เท็มเพลตแท็บแอปพลิเคชั้น** ให้เลือก **จัดการ**
1. สร้างแท็บแอปลิเคชันใหม่ ของชนิด **เว็บไซต์ของบุคคลที่สาม** สำหรับคำแนะนำ ให้ดู [จัดการเท็มเพลตแท็บแอปพลิเคชัน](/dynamics365/app-profile-manager/application-tab-templates?tabs=customerserviceadmincenter)
1. ภายใต้ **พารามิเตอร์** ในฟิลด์ **ค่า** ของพารามิเตอร์ **url** ให้ป้อน URL ต่อไปนี้ โดยที่ `<YourOrganizationHeadquartersURL>` และ `<LegalEntityname>` ถูกแทนที่ด้วยค่าที่เหมาะสม บริการลูกค้าของช่องทาง Omni อ่าน **{AccountNumber}** จากบริบทการสนทนา ดังนั้น ให้ปล่อย **{AccountNumber}** ตามที่เป็นอยู่

    `https://<YourOrganizationHeadquartersURL>/?mi=MCRCustomerService&cmp=<LegalEntityName>&embedded=true&customerId={AccountNumber}`

1. ปล่อยให้ฟิลด์ **ค่า** ของพารามิเตอร์ **ข้อมูล** ว่างเปล่า

![การสร้างแท็บแอปลิเคชันใน Dynamics 365 Omnichannel Customer Service](media/OC-CS-Admin-Application-Tab-Parameters.png)

## <a name="enable-a-new-application-tab-for-customer-agents-in-dynamics-365-omnichannel-for-customer-service"></a>เปิดใช้งานแท็บแอปพลิเคชันใหม่สำหรับตัวแทนลูกค้า ใน Dynamics 365 Omnichannel for Customer Service

ในการเปิดใช้งานแท็บแอปพลิเคชันใหม่สำหรับตัวแทนลูกค้า ใน Dynamics 365 Omnichannel for Customer Service ให้ทำตามขั้นตอนเหล่านี้
    
1. เปิด [Power Apps Maker Portal](https://make.powerapps.com)
1. ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **Apps**
1. เลือก **ศูนย์การจัดการ Customer Service**
1. ไปที่ **ฝ่ายสนับสนุนลูกค้า \> สตรีมงาน**
1. เปิดสตรีมงานที่คุณสร้างขึ้นให้กับตัวแทนของคุณ จากนั้นภายใต้ **การตั้งค่าขั้นสูง** ให้เลือก **รอบเวลาเริ่มต้น**
1. ภายใต้ **แท็บแอปลิเคชัน** ให้เลือก **เพิ่มแท็บแอปลิเคชันที่มีอยู่** แล้วเพิ่มแท็บแอปลิเคชันใหม่ที่คุณสร้างขึ้นก่อนหน้านี้ ขั้นตอนนี้ช่วยให้มั่นใจว่าแท็บแอปลิเคชันที่โหลด Commerce headquarters ในโมดูล iFrame จะปรากฏขึ้นเมื่อตัวแทนรับการสนทนาขาเข้าจากเว็บไซต์อีคอมเมิร์ซของคุณ

## <a name="add-context-variables-in-dynamics-365-omnichannel-for-customer-service"></a>เพิ่มตัวแปรบริบทใน Dynamics 365 Omnichannel for Customer Service

การเพิ่มตัวแปรบริบทใน Dynamics 365 Omnichannel for Customer Service ให้ทำตามขั้นตอนเหล่านี้

1. เปิด [Power Apps Maker Portal](https://make.powerapps.com)
1. ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **Apps**
1. เลือก **ศูนย์การจัดการ Customer Service**
1. ไปที่ **ฝ่ายสนับสนุนลูกค้า \> สตรีมงาน**
1. เปิดสตรีมงานที่คุณสร้างขึ้นให้กับตัวแทนของคุณ จากนั้นภายใต้ **การตั้งค่าขั้นสูง** ให้ไปที่ส่วน **ตัวแปรบริบท**
1. เลือก **แก้ไข** แล้วเพิ่ม **AccountNumber** เป็นตัวแปรบริบท ของขนิด **ข้อความ** ตัวแปรนี้จะช่วย Commerce Headquarters โหลดข้อมูลของลูกค้าด้วยหมายเลขบัญชีที่ตรงกัน

> [!NOTE]
> หากคุณต้องการอ่านที่อยู่อีเมลและชื่อของผู้ใช้ที่ลงชื่อเข้าใช้จากช่องทางอีคอมเมิร์ซ คุณสามารถเพิ่ม **อีเมล** และ **ชื่อ** เป็นตัวแปรบริบทของชนิด **ข้อความ** ได้นอกเหนือจากตัวแปรบริบท **AccountNumber**
