---
title: คำนวณความพร้อมของสินค้าคงคลังสำหรับช่องทางการขายปลีก
description: หัวข้อนี้จะอธิบายถึงตัวเลือกที่พร้อมใช้งานสำหรับการแสดงสินค้าคงคลังคงเหลือสำหรับช่องทางร้านค้าและออนไลน์
author: hhainesms
manager: annbe
ms.date: 08/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 68fa26daac055cd0fd72035683f05ed36052b3a3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995831"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>คำนวณความพร้อมของสินค้าคงคลังสำหรับช่องทางการขายปลีก

[!include [banner](../includes/banner.md)]

หัวข้อนี้จะอธิบายวิธีการที่บริษัทสามารถใช้ Microsoft Dynamics 365 Commerce เพื่อดูความพร้อมของสินค้าคงคลังคงเหลือที่ประเมินไว้สำหรับผลิตภัณฑ์ในช่องทางออนไลน์และร้านค้า

## <a name="accuracy-of-calculation"></a>ความถูกต้องของการคำนวณ

Commerce ใช้เซิร์ฟเวอร์และฐานข้อมูลจำนวนมากเพื่อให้แน่ใจว่ามีการขยายและประสิทธิภาพการทำงาน ดังนั้น จึงเป็นเรื่องสำคัญอย่างยิ่งที่คุณเข้าใจว่ามูลค่าสินค้าคงคลังที่พร้อมใช้งานที่ได้รับมาจากแอพลิเคชันการขายหน้าร้าน (POS) แอพลิเคชันโปรแกรมมิ่งอินเทอร์เฟสของความพร้อมของสินค้าคงคลังอีคอมเมิร์ซ และหน้าสินค้าคงคลังคงเหลือในศูนย์ควบคุม Commerce อาจไม่ถูกต้อง 100 เปอร์เซ็นต์ในเวลาจริง ถ้าธุรกรรมที่สร้างขึ้นสำหรับผลิตภัณฑ์ในช่องทางออนไลน์หรือร้านค้ายังไม่ได้ซิงค์กับเซิร์ฟเวอร์ศูนย์ควบคุม Commerce และฐานข้อมูล หน้าสินค้าคงคลังคงเหลือในศูนย์ควบคุม Commerce อาจไม่แสดงมูลค่าสินค้าคงคลังตามเวลาจริงที่ถูกต้องสำหรับผลิตภัณฑ์ดังกล่าว ตรงกันข้าม ถ้าคุณได้ตั้งค่าคอนฟิกบริษัทของคุณเพื่อให้ผู้ใช้ในศูนย์ควบคุม Commerce หรือแอพลิเคชันแบบรวมอื่นๆ สามารถขาย ได้รับ ส่งคืน หรือปรับปรุงสินค้าคงคลังออกจากร้านค้าหรือคลังสินค้าออนไลน์ ช่องทาง POS หรือออนไลน์อาจไม่มีข้อมูลทั้งหมดที่จำเป็นสำหรับการแสดงค่าคงเหลือในเวลาจริงที่ถูกต้องสำหรับสินค้า

หัวข้อนี้จะอธิบายกระบวนการซิงโครไนส์ข้อมูลที่สามารถรันได้บ่อยครั้ง เพื่อช่วยจำกัดเวลาแฝงของข้อมูลระหว่างแอพลิเคชันหรือช่องทาง อย่างไรก็ตาม คุณควรเข้าใจว่าข้อมูลความพร้อมใช้งานคงเหลือทั้งหมดที่ระบุไว้ในระหว่างวันดำเนินงานถือเป็นมูลค่าที่ประมาณการไว้ ดังนั้น ถ้าคุณพยายามที่จะเปรียบเทียบข้อมูลสินค้าคงคลังคงเหลือที่แอพลิเคชันให้พร้อมกับสินค้าคงคลังทางกายภาพจริงบนชั้นวาง หรือหากคุณพยายามที่จะเปรียบเทียบค่าคงเหลือที่แสดงอยู่ใน POS โดยมีข้อมูลคงเหลือที่คุณค้นหาสำหรับคลังสินค้าเดียวกันในศูนย์ควบคุม Commerce ค่าอาจแตกต่างกัน ความแตกต่างนี้ในระหว่างวันดำเนินงานถูกคาดไว้และไม่ควรมีการพิจารณาถึงปัญหา ถ้าคุณต้องการตรวจสอบความถูกต้องของข้อมูลและตรวจสอบให้แน่ใจว่าค่าที่ระบุไว้ใน APIs ความพร้อมใช้งานของสินค้าคงคลังและศูนย์ควบคุม Commerce จะจับคู่หน่วยทางกายภาพจริงที่คุณพบในร้านค้าหรือชั้นคลังสินค้าของคุณ เวลาที่ดีที่สุดในการทำเช่นนั้นคือหลังจากการดำเนินการของช่องทางได้หยุดทำงานสำหรับวันนั้น และธุรกรรมทั้งหมดถูกซิงค์ระหว่างศูนย์ควบคุม Commerce และช่องทางอย่างถูกต้อง

## <a name="use-inventory-lookup-apis-for-e-commerce-inventory-availability-requests"></a>ใช้ APIs การค้นหาสินค้าคงคลังสำหรับการร้องขอความพร้อมใช้งานของสินค้าคงคลังของพาณิชย์อิเล็กทรอนิกส์

คุณสามารถใช้ APIs ต่อไปนี้เพื่อแสดงความพร้อมใช้งานของสินค้าคงคลังสำหรับผลิตภัณฑ์ เมื่อลูกค้าของคุณมีการซื้อสินค้าบนไซต์อีคอมเมิร์ซ

- **GetEstimatedAvailability** – ใช้ API นี้เพื่อเรียกดูความพร้อมของสินค้าคงคลังสำหรับสินค้าในคลังสินค้าของช่องทางอีคอมเมิร์ซ หรือคลังสินค้าทั้งหมดที่เชื่อมโยงกับการตั้งค่าคอนฟิกของกลุ่มการเติมสินค้าสำหรับช่องทางอีคอมเมิร์ซ นอกจากนี้ คุณยังสามารถใช้ API นี้สำหรับคลังสินค้าในพื้นที่การค้นหาหรือรัศมีเฉพาะ โดยยึดตามข้อมูลลองจิจูดและละติจูดได้อีกด้วย
- **GetEstimatedProductWarehouseAvailability** – ใช้ API นี้เพื่อร้องขอสินค้าคงคลังสำหรับสินค้าจากคลังสินค้าหนึ่งๆ ตัวอย่างเช่น คุณสามารถใช้เพื่อแสดงความพร้อมใช้งานของสินค้าคงคลังในสถานการณ์ที่เกี่ยวข้องกับการเบิกสินค้าตามใบสั่ง

> [!NOTE]
> APIs เหล่านี้จะแทนที่ APIs ของ **GetProductAvailabilities** และ **GetAvailableInventoryNearby** ใน Dynamics 365 Retail รุ่น10.0.7 และก่อนหน้านี้

APIs ทั้งสองดึงข้อมูลจากเซิร์ฟเวอร์ Commerce และให้ค่าประเมินของสินค้าคงคลังคงเหลือสำหรับชุดเฉพาะของผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยและคลังสินค้า ถึงแม้ว่า APIs อื่นๆ ที่มีอยู่บนเซิร์ฟเวอร์ Commerce สามารถไปยังศูนย์ควบคุม Commerce ได้โดยตรงเพื่อดึงปริมาณคงเหลือสำหรับผลิตภัณฑ์ เราไม่แนะนำให้มีการใช้งานในสภาพแวดล้อมของอีคอมเมิร์ซ เนื่องจากปัญหาประสิทธิภาพที่อาจเกิดขึ้นและผลกระทบที่เกี่ยวข้องที่คำขอบ่อยครั้งเหล่านี้อาจมีอยู่บนเซิร์ฟเวอร์ศูนย์ควบคุม Commerce นอกจากนี้ ถ้ามีการคำนวณสินค้าคงคลังคงเหลือผ่านเซิร์ฟเวอร์ Commerce การคำนวณมีแนวโน้มที่จะรวมสินค้าคงคลังที่ถูกขายในธุรกรรมอีคอมเมิร์ซล่าสุดที่ยังไม่ได้ซิงค์กับศูนย์ควบคุม Commerce ถึงแม้ว่าศูนย์ควบคุม Commerce อาจไม่มีข้อมูลเกี่ยวกับธุรกรรมเหล่านี้ เซิร์ฟเวอร์ Commerce และฐานข้อมูลข่องทางนั้นมีข้อมูล ดังนั้น ข้อมูลจะถูกรวมเข้าไปและสามารถช่วยให้มีการประเมินสินค้าคงคลังที่พร้อมใช้งานของผลิตภัณฑ์ที่มีความถูกต้องมากขึ้น

### <a name="get-started-with-e-commerce-calculated-inventory-availability"></a>เริ่มต้นใช้งานสินค้าคงคลังที่มีการคำนวณของอีคอมเมิร์ซ

ก่อนที่คุณจะใช้ API สองรายการที่ได้กล่าวถึงก่อนหน้านี้ คุณต้องเปิดใช้งานคุณลักษณะ **การคำนวณความพร้อมใช้งานของผลิตภัณฑ์ที่ปรับให้เหมาะสม** ผ่านพื้นที่ทำงาน **การจัดการคุณลักษณะ** ในศูนย์ควบคุม Commerce

ก่อนที่ APIs จะสามารถคำนวณการประเมินที่ดีที่สุดของความพร้อมใช้งานของสินค้าคงคลังสำหรับสินค้าหนึ่งๆ จะต้องมีการประมวลผลสแนปช็อตของความพร้อมใช้งานของสินค้าคงคลังเป็นครั้งคราวจากศูนย์ควบคุม Commerce และส่งไปยังฐานข้อมูลช่องทางที่ Commerce Scale Unit ของอีคอมเมิร์ซใช้ สแนปช็อตแสดงถึงข้อมูลที่ศูนย์ควบคุม Commerce มีเกี่ยวกับความพร้อมของสินค้าคงคลังสำหรับชุดที่กำหนดของผลิตภัณฑ์หรือผลิตภัณฑ์ย่อยและคลังสินค้า ซึ่งอาจรวมถึงการปรับปรุงหรือการเคลื่อนไหวของสินค้าคงคลังที่เกิดขึ้นจากการรับสินค้าคงคลัง หรือโดยการจัดส่งหรือกระบวนการอื่นๆ ที่มีการดำเนินการในศูนย์ควบคุม Commerce และที่ช่องทางอีคอมเมิร์ซมีข้อมูลที่เกี่ยวข้องเนื่องเนื่องจากกระบวนการซิงโครไนส์เท่านั้น

สแนปช็อตฐานข้อมูลที่งาน **ความพร้อมใช้งานของผลิตภัณฑ์** จะคำนวณเฉพาะธุรกรรมสินค้าคงคลังที่มีการประมวลผลและลงรายการบัญชีในศูนย์ควบคุม Commerce เมื่อมีการดำเนินการสแนปช็อตเท่านั้น ถ้ามีการขายสินค้าคงคลังสำหรับผลิตภัณฑ์ในคลังสินค้าของร้านค้าผ่านทางการขายที่มีการชำระเงินด้วยเงินสดและการดำเนินการในใบสั่งของลูกค้าแบบอะซิงโครนัสในแอพลิเคชัน POS ศูนย์ควบคุม Commerce จะไม่มีข้อมูลเกี่ยวกับธุรกรรมการออกใช้สินค้าคงคลังที่เกี่ยวข้องสำหรับการขายในทันที ซึ่งจะมีข้อมูลเกี่ยวกับสินค้าคงคลังที่ขายสำหรับชนิดของการขายร้านค้าเหล่านี้เท่านั้น หลังจากงาน P อัพโหลดธุรกรรมที่เกี่ยวข้องจากฐานข้อมูลช่องทางของร้านค้าเข้าสู่ศูนย์ควบคุม Commerce และใบสั่งขายที่เกี่ยวข้องจะถูกสร้างขึ้นผ่านการลงรายการบัญชีใบแจ้งยอดหรือกระบวนการลงรายการบัญชีของฟีดแบบต่อเนื่อง กระบวนการในการสร้างใบสั่งในศูนย์ควบคุม Commerce จะสร้างธุรกรรมสินค้าคงคลังที่เกี่ยวข้อง สำหรับใบสั่งของช่องทางอีคอมเมิร์ซ ศูนย์ควบคุม Commerce มีข้อมูลเกี่ยวกับธุรกรรมสินค้าคงคลังเฉพาะหลังจากที่ธุรกรรมถูกส่งไปยังศูนย์ควบคุม Commerce ผ่านงาน P และกระบวนการซิงโครไนส์ใบสั่งเสร็จสมบูรณ์แล้ว ดังนั้น จึงเป็นเรื่องสำคัญอย่างยิ่งที่คุณเข้าใจว่าค่าสแนปช็อตของสินค้าคงคลังที่ระบุไว้ในงาน **ความพร้อมใช้งานของผลิตภัณฑ์** อาจไม่ถูกต้อง 100 เปอร์เซ็นต์ในเวลาจริง เนื่องจากมีการประมวลผลยอดขายคงที่ที่เกิดขึ้นในเซิร์ฟเวอร์แบบกระจาย

เมื่อต้องการใช้สแนปช็อตของสินค้าคงคลังในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนเหล่านี้

1. ไปที่ **Retail และ Commerce \> Retail และ Commerce IT \> ผลิตภัณฑ์และสินค้าคงคลัง \> ความพร้อมใช้งานของผลิตภัณฑ์**
1. เลือก **ตกลง** เพื่อรันงาน **ความพร้อมใช้งานของผลิตภัณฑ์** นอกจากนี้ คุณยังสามารถจัดกำหนดการงานนี้เพื่อให้รันในชุดงานได้ด้วย

หลังจากที่งาน **ความพร้อมใช้งานของผลิตภัณฑ์** เสร็จสิ้นการรันแล้ว ข้อมูลที่ถูกบันทึกต้องถูกผลักดันให้กับฐานข้อมูลช่องทางอีคอมเมิร์ซ เพื่อให้มีการพิจารณาสแนปช็อตสินค้าคงคลังของศูนย์ควบคุม Commerce ล่าสุดอยู่ในการคำนวณสินค้าคงคลังคงเหลือที่มีการประเมิน

1. ไปยัง **การขายปลีกและการค้า \> การขายปลีกและไอทีเชิงพาณิชย์ \> กำหนดการการจัดจำหน่าย**
1. รันงาน **1130** (**ความพร้อมใช้งานของผลิตภัณฑ์**) เพื่อซิงค์ข้อมูลสแนปช็อตที่งาน **ความพร้อมใช้งานของผลิตภัณฑ์** สร้างขึ้นจากศูนย์ควบคุม Commerce ไปยังฐานข้อมูลช่องทางของคุณ

เมื่อมีการร้องขอความพร้อมของสินค้าคงคลังจาก API ของ **GetEstimatedAvailability** หรือ **GetEstimatedProductWarehouseAvailability** จะมีการดำเนินการคำนวณเพื่อลองใช้การประเมินสินค้าคงคลังที่เป็นไปได้ที่ดีที่สุดสำหรับผลิตภัณฑ์ การคำนวณจะอ้างอิงถึงใบสั่งของลูกค้าอีคอมเมิร์ซใดๆ ที่อยู่ในฐานข้อมูลช่องทาง แต่ไม่ได้รวมอยู่ในข้อมูลสแนปช็อตที่มีงาน 1130 ระบุ ตรรกะนี้ดำเนินการโดยการติดตามธุรกรรมสินค้าคงคลังที่ประมวลผลล่าสุดจากศูนย์ควบคุม Commerce และการเปรียบเทียบกับธุรกรรมในฐานข้อมูลช่องทาง ซึ่งจะให้ข้อมูลพื้นฐานสำหรับตรรกะการคำนวณด้านข้างช่องทาง เพื่อให้การเคลื่อนย้ายสินค้าคงคลังเพิ่มเติมที่เกิดขึ้นสำหรับธุรกรรมการขายของใบสั่งของลูกค้าในฐานข้อมูลช่องทางอีคอมเมิร์ซสามารถถูกรวมเป็นมูลค่าสินค้าคงคลังที่ประมาณการไว้ซึ่ง API ระบุ

ตรรกะการคำนวณด้านข้างช่องทางจะส่งคืนค่าที่มีอยู่จริงโดยประมาณและค่าที่พร้อมใช้งานทั้งหมดสำหรับผลิตภัณฑ์และคลังสินค้าที่ร้องขอ คุณสามารถแสดงค่าบนไซต์อีคอมเมิร์ซของคุณ ถ้าคุณต้องการ หรือสามารถใช้เพื่อทริกเกอร์ตรรกะทางธุรกิจอื่นๆ บนไซต์อีคอมเมิร์ซของคุณได้ ตัวอย่างเช่น คุณสามารถแสดงข้อความ "ไม่มีสินค้าในสต็อก" แทนปริมาณคงเหลือจริงที่ API ผ่าน

ตรรกะการคำนวณที่ใช้ APIs ของอีคอมเมิร์ซด้านช่องทางสำหรับมูลค่าสินค้าคงคลังโดยประมาณ สามารถประเมินสินค้าคงคลังตามใบสั่งของลูกค้าที่ได้ถูกสร้างขึ้นในฐานข้อมูลช่องทางเท่านั้น แต่ยังไม่ได้ถูกซิงค์และลงรายการบัญชีในศูนย์ควบคุม Commerce นอกจากนี้ ถ้าฐานข้อมูลช่องทางของคุณมีข้อมูลธุรกรรมสำหรับการขายเงินสดและการขนส่งสำหรับคลังสินค้าเฉพาะร้านค้า จะไม่มีการรวมการขายเงินสดและการขนส่งในการคำนวณอีคอมเมิร์ซด้านช่องทางสำหรับคลังสินค้าเหล่านั้น

## <a name="configure-the-inventory-lookup-operation-in-the-pos-channel"></a>ตั้งค่าคอนฟิกการดำเนินการค้นหาสินค้าคงคลังในช่องทาง POS

ใน Retail รุ่น 10.0.9 และรุ่นก่อนหน้า การดำเนินการ **การค้นหาสินค้าคงคลัง** จาก POS ใช้การเรียกบริการแบบเรียลไทมไปยังศูนย์ควบคุม Commerce เพื่อเรียกดูข้อมูลสินค้าคงคลังสำหรับผลิตภัณฑ์ที่เลือกสำหรับทั้งร้านค้าปัจจุบันของผู้ใช้และร้านค้าอื่นๆ ที่มีการตั้งค่าคอนฟิกสำหรับกลุ่มการเติมสินค้าเป็นส่วนหนึ่งของการตั้งค่าคอนฟิกช่องทางสำหรับร้านค้า ใน Commerce รุ่น10.0.10 และรุ่นที่ใหม่กว่า คุณสามารถปิดใช้งานการเรียกบริการแบบเรียลไทม์ไปยังศูนย์ควบคุม Commerce ได้ แต่คุณสามารถใช้การคำนวณด้านข้างช่องทางบนเซิร์ฟเวอร์ Commerce เพื่อกำหนดสินค้าคงคลังคงเหลือที่พร้อมใช้งานทางกายภาพสำหรับร้านค้าและที่ตั้งอื่นๆ ที่กำหนดไว้ในกลุ่มการเติมสินค้า นอกจากนี้ การตั้งค่าคอนฟิกสินค้าคงคลังที่คำนวณโดยช่องทางนี้ยังมีประโยชน์สำหรับสถานที่ซึ่งการเชื่อมต่ออินเทอร์เน็ตไม่น่าเชื่อถือ เนื่องจากคุณไม่จำเป็นต้องออนไลน์เพื่อเรียกการค้นหาสินค้าคงคลังจากศูนย์ควบคุม Commerce

เมื่อการคำนวณด้านข้างช่องทางได้รับการตั้งค่าคอนฟิกและมีการจัดการอย่างถูกต้อง จึงสามารถให้การประเมินที่น่าเชื่อถือมากขึ้นของสินค้าคงคลังของร้านค้าปัจจุบัน เนื่องจากมีการใช้ข้อมูลธุรกรรมที่อยู่ในฐานข้อมูลช่องทาง Commerce แต่ศูนย์ควบคุม Commerce อาจยังไม่มีข้อมูลที่เกี่ยวข้อง ตัวอย่างเช่น ถ้าคุณใช้การเรียกบริการแบบเรียลไทม์ที่มีอยู่สำหรับการค้นหาสินค้าคงคลังใน POS ศูนย์ควบคุม Commerce อาจจะยังไม่มีข้อมูลเกี่ยวกับการขายเงินสดและการขนส่งที่เพิ่งเกิดขึ้นสำหรับผลิตภัณฑ์ ดังนั้น ค่าสินค้าคงคลังคงเหลือที่ศูนย์ควบคุม Commerce ส่งคืนสำหรับผลิตภัณฑ์ดังกล่าวอาจจะเกินสินค้าคงคลังคงเหลือจริงของร้านค้าหนึ่งหน่วย อย่างไรก็ตาม ถ้าคุณใช้การคำนวณด้านข้างช่องทาง การขายแบบเงินสดและการขนส่งจะถูกรวมเป็นการคำนวณและหักจากมูลค่าคงเหลือที่แสดงไว้ ถึงแม้ว่าค่าที่ทั้งการคำนวณด้านช่องทางและการเรียกบริการแบบเรียลไทม์มีให้นั้นเป็นการประเมินสินค้าคงคลังคงเหลือเท่านั้น ค่าที่การคำนวณด้านช่องทางมีให้นั้นมีแนวโน้มที่จะถูกต้องมากกว่าสำหรับร้านค้าปัจจุบัน

### <a name="get-started-with-pos-channel-side-calculated-inventory-availability"></a>เริ่มต้นใช้งานความพร้อมของสินค้าคงคลังที่มีการคำนวณด้านข้างช่องทาง POS

เมื่อต้องการใช้ตรรกะการคำนวณฝั่งช่องทางและปิดใช้งานการเรียกบริการแบบเรียลไทม์สำหรับการค้นหาสินค้าคงคลังจากแอปพลิเคชัน POS อันดับแรกคุณต้องเปิดใช้งานคุณลักษณะ **การคำนวณความพร้อมของผลิตภัณฑ์ที่ปรับให้เหมาะสม** ผ่านพื้นที่ทำงาน **การจัดการคุณลักษณะ** ในศูนย์ควบคุม Commerce นอกจากการเปิดใช้งานคุณลักษณะแล้ว คุณต้องทำการเปลี่ยนแปลงไปยัง **โพรไฟล์ฟังก์ชันการทำงาน**

เมื่อต้องการเปลี่ยนแปลง **โพรไฟล์ฟังก์ชันการทำงาน** ให้ทำตามขั้นตอนเหล่านี้:

1. ไปที่ **การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> การตั้งค่า POS \> โพรไฟล์POS \> โพรไฟล์ฟังก์ชัน**
1. เลือกโพรไฟล์ฟังก์ชัน
1. บน FastTab **ฟังก์ชัน** ในส่วน **การคำนวณความพร้อมใช้งานของสินค้าคงคลัง** ให้เปลี่ยนค่าของฟิลด์ **โหมดการคำนวณความพร้อมใช้งานของสินค้าคงคลัง** จาก **บริการแบบเรียลไทม์** เป็น **ช่องทาง** โดยค่าเริ่มต้น โพรไฟล์ฟังก์ชันทั้งหมดใช้การเรียกบริการแบบเรียลไทม์ ดังนั้น คุณต้องเปลี่ยนค่าของฟิลด์นี้ ถ้าคุณต้องการใช้ตรรกะการคำนวณด้านข้างช่องทาง ร้านค้าปลีกทั้งหมดที่เชื่อมโยงกับโพรไฟล์ฟังก์ชันที่เลือกจะได้รับผลกระทบจากการเปลี่ยนแปลงนี้

จากนั้น คุณต้องซิงค์การเปลี่ยนแปลงกับช่องทางผ่านกระบวนการจัดกำหนดการกระจาย โดยดำเนินการตามขั้นตอนต่อไปนี้:

1. ไปยัง **การขายปลีกและการค้า \> การขายปลีกและไอทีเชิงพาณิชย์ \> กำหนดการการจัดจำหน่าย**
1. รันงาน **1070** (**การตั้งค่าคอนฟิกช่องทาง**)

หลังจากที่การตั้งค่าคอนฟิกเสร็จสมบูรณ์ ข้อมูลที่ระบุเกี่ยวกับสินค้าคงคลังที่มีอยู่จริงจะไม่มีการใช้การเรียกบริการแบบเรียลไทม์อีกต่อไป เมื่อผู้ใช้ในแอพลิเคชัน POS ใช้การดำเนินการ **การค้นหาสินค้าคงคลัง** (มุมมองมาตรฐานและเมทริกซ์) แต่ข้อมูลเกี่ยวกับสินค้าคงคลังที่มีอยู่จริงสำหรับร้านค้าปัจจุบันและร้านค้าทั้งหมดในกลุ่มการเติมสินค้าจะถูกคำนวณตามสแนปช็อตที่รู้จักล่าสุด ซึ่งถูกจัดส่งไปยังฐานข้อมูลช่องทางจากศูนย์ควบคุม Commerce ค่าสแนปช็อตมีการจำกัดเพิ่มเติมโดยการคำนวณด้านของช่องทางเพื่อปรับปรุงค่าที่มีอยู่จริง ตามธุรกรรมการขายหรือการส่งคืนเพิ่มเติมที่มีอยู่สำหรับผลิตภัณฑ์ที่เลือกไว้ในฐานข้อมูลช่องทางที่ไม่ได้รวมอยู่ในสแนปช็อตที่มีการซิงโครไนส์ล่าสุดจากงาน 1130 ถ้าฐานข้อมูลช่องทางไม่มีข้อมูลธุรกรรมสำหรับคลังสินค้าหรือร้านค้าใดๆ ในกลุ่มการเติมสินค้า จะไม่มีธุรกรรมเพิ่มเติมที่สามารถรวมเป็นการคำนวณค่าอีกครั้งได้ ดังนั้น การประเมินสินค้าคงคลังคงเหลือที่ดีที่สุดที่สามารถแสดงได้สำหรับคลังสินค้าหรือร้านค้าเหล่านั้นคือ ข้อมูลจากสแนปช็อตของศูนย์ควบคุม Commerce ที่รู้จักล่าสุด

หน้าจอ **การเติมสินค้าตามใบสั่ง** ของ POS ยังใช้ประโยชน์จากการคำนวณด้านของช่องทางเพื่อแสดงสินค้าคงคลังคงเหลือสำหรับสินค้า เมื่อมีการเลือกรายการการเติมสินค้าของใบสั่ง และผู้ใช้ดูแผง **รายละเอียด** สำหรับสินค้าคงคลังคงเหลือสำหรับสินค้าที่เลือก

## <a name="optimize-your-inventory-data"></a>เพิ่มประสิทธิภาพข้อมูลสินค้าคงคลังของคุณ

เพื่อให้แน่ใจในการประเมินสินค้าคงคลังเป็นไปได้ที่ดีที่สุด จึงเป็นเรื่องสำคัญอย่างยิ่งที่คุณจะใช้ชุดงาน Commerce ต่อไปนี้ และรันชุดงานเหล่านี้บ่อยครั้ง:

- **งาน P** – พบงาน P บนหน้า **กำหนดการกระจาย** และควรรันบ่อยๆ งานนี้จะนำใบสั่งอีคอมเมิร์ซ ใบสั่งของลูกค้าแบบอะซิงโครนัสที่มีการสร้าง POS และใบสั่งเงินสดและการขนส่งที่ POS สร้างขึ้นจากฐานข้อมูลช่องทางเข้าสู่ศูนย์ควบคุม Commerce เพื่อให้สามารถดำเนินการต่อได้ จนกว่าข้อมูลนี้จะถูกซิงค์จากช่องทางไปยังศูนย์ควบคุม Commerce ศูนย์ควบคุม Commerce ไม่มีข้อมูลเกี่ยวกับการปรับปรุงสินค้าคงคลังให้กับผลิตภัณฑ์ในคลังสินค้าที่เป็นผลมาจากธุรกรรมดังกล่าว
- **ซิงโครไนส์ใบสั่ง** – งานนี้จะประมวลผลข้อมูลของธุรกรรมดิบในศูนย์ควบคุม Commerce ซึ่งงาน P มีให้และแปลงธุรกรรมใบสั่งซื้อของลูกค้าและแบบอะซิงโครนัสให้เป็นใบสั่งขายในศูนย์ควบคุม Commerce จนกว่าจะมีการประมวลผลงานนี้และใบสั่งขายถูกสร้างขึ้น จะไม่มีการสร้างธุรกรรมสินค้าคงคลัง ดังนั้น สินค้าคงคลังคงเหลือในศูนย์ควบคุม Commerce จะไม่พิจารณาธุรกรรม
- **คำนวณใบแจ้งยอดธุรกรรมเป็นชุดงาน** – สำหรับธุรกรรมเงินสดและการขนส่งที่สร้างขึ้นในร้านค้า กระบวนการลงรายการบัญชีฟีดแบบต่อเนื่องช่วยให้มั่นใจว่าสินค้าคงคลังที่เกี่ยวข้องกับการขายจะถูกปรับปรุงอย่างมีประสิทธิภาพ เมื่อต้องการได้รับการประมวลผลที่มีประสิทธิภาพสูงสุดของธุรกรรมสินค้าคงคลังสำหรับใบสั่งแบบเงินสดและการขนส่ง ตรวจสอบให้แน่ใจว่าคุณตั้งค่าคอนฟิกระบบของคุณให้ใช้ [การลงรายการบัญชีฟีดแบบต่อเนื่อง](https://docs.microsoft.com/dynamics365/commerce/trickle-feed)
- **ลงรายการบัญชีใบแจ้งยอดธุรกรรมเป็นชุดงาน** – งานนี้ยังต้องใช้สำหรับการลงรายการบัญชีฟีดแบบต่อเนื่องอีกด้วย นี่จะเป็นไปตามงาน **คำนวณใบแจ้งยอดธุรกรรมเป็นชุดงาน** งานนี้จะลงรายการบัญชีใบแจ้งยอดที่มีการคำนวณอย่างเป็นระบบ ดังนั้นจึงมีการสร้างใบสั่งขายสำหรับการขายแบบเงินสดและการขนส่งในศูนย์ควบคุม Commerce และศูนย์ควบคุม Commerce จะสะท้อนถึงสินค้าคงคลังของร้านค้าของคุณได้อย่างถูกต้องมากขึ้น
- **ความพร้อมใช้งานของผลิตภัณฑ์** – งานนี้สร้างสแนปช็อตของสินค้าคงคลังจากศูนย์ควบคุม Commerce
- **1130 (ความพร้อมใช้งานของผลิตภัณฑ์)** – งานนี้พบบนหน้า **กำหนดการกระจาย** และควรรันทันทีหลังจากงาน **ความพร้อมใช้งานของผลิตภัณฑ์** งานนี้จะขนส่งข้อมูลสแนปช็อตของสินค้าคงคลังจากศูนย์ควบคุม Commerce ไปยังฐานข้อมูลช่องทาง

ขอแนะนำว่าคุณไม่ควรรันชุดงานเหล่านั้นบ่อยเกินไป (ทุกสองสามนาที) การเรียกใช้งานบ่อยครั้งจะทำให้ศูนย์ควบคุม Commerce (HQ) ทำงานหนักเกินไปและอาจส่งผลต่อประสิทธิภาพการทำงาน โดยทั่วไปแล้ว ควรมีการตรวจสอบความพร้อมของผลิตภัณฑ์และงาน 1130 เป็นรายชั่วโมง และจัดกำหนดการงาน P, ซิงโครไนส์ใบสั่ง และงานที่เกี่ยวข้องกับการลงรายการบัญชีขตามฟีดแบบต่อเนื่องด้วยความถี่เดียวกันหรือสูงกว่า

> [!NOTE]
> สำหรับเหตุผลด้านประสิทธิภาพการทำงาน เมื่อมีการใช้การคำนวณความพร้อมของสินค้าคงคลังด้านข้างช่องทางเพื่อทำให้มีการร้องขอความพร้อมใช้งานของสินค้าคงคลังโดยใช้API พาณิชย์อิเล็กทรอนิกส์หรือตรรกะสินค้าคงคลังด้านข้างช่องทางของ POS ใหม่ การคำนวณจะใช้แคชเพื่อกำหนดว่าเวลาที่เพียงพอได้ส่งผ่านเพื่อตรวจสอบการรันตรรกะการคำนวณอีกครั้งหรือไม่ แคชเริ่มต้นถูกตั้งค่าเป็น 60 วินาที ตัวอย่างเช่น คุณเปิดการคำนวณด้านข้างช่องทางสำหรับร้านค้าของคุณและดูสินค้าคงคลังคงเหลือสำหรับผลิตภัณฑ์บนหน้า **การค้นหาสินค้าคงคลัง** ถ้ามีการขายผลิตภัณฑ์หนึ่งหน่วยขึ้นไป หน้า **การค้นหาสินค้าคงคลัง** จะไม่แสดงสินค้าคงคลังที่ลดลงจนกว่าแคชจะถูกล้างข้อมูล หลังจากที่ผู้ใช้ลงรายการบัญชีธุรกรรมใน POS แล้ว พวกเขาควรรอ 60 วินาที ก่อนที่พวกเขาจะตรวจสอบว่าสินค้าคงคลังคงเหลือลดลงแล้วหรือไม่

ถ้าสถานการณ์จำลองทางธุรกิจของคุณต้องการเวลาแคชที่น้อยลง โปรดติดต่อเจ้าหน้าที่ฝ่ายสนับสนุนผลิตภัณฑ์ของคุณเพื่อขอความช่วยเหลือ
