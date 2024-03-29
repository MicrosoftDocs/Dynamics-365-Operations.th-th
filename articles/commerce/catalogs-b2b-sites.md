---
title: สร้างแค็ตตาล็อก Commerce สำหรับไซต์ B2B
description: บทความนี้อธิบายวิธีการสร้างแค็ตตาล็อก Commerce สำหรับไซต์แบบธุรกิจกับธุรกิจ (B2B) ของ Microsoft Dynamics 365 Commerce
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 7d4ed3e2a76924c2c3c0ba55e21ba648e8da7b76
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136838"
---
# <a name="create-commerce-catalogs-for-b2b-sites"></a>สร้างแค็ตตาล็อก Commerce สำหรับไซต์ B2B

[!include [banner](includes/banner.md)]

บทความนี้อธิบายวิธีการสร้างแค็ตตาล็อกผลิตภัณฑ์ Commerce สำหรับไซต์แบบธุรกิจกับธุรกิจ (B2B) ของ Microsoft Dynamics 365 Commerce หากต้องการทราบคําตอบของคําถามที่ถามบ่อยเกี่ยวกับแค็ตตาล็อก Commerce สำหรับไซต์ B2B ดูที่ [คำถามที่ถามบ่อยเกี่ยวกับแค็ตตาล็อก Commerce สำหรับ B2B](catalogs-b2b-sites-FAQ.md)

> [!NOTE]
> บทความนี้ใช้กับ Dynamics 365 Commerce รุ่น 10.0.27 และรุ่นที่ใหม่กว่า

คุณสามารถใช้แค็ตตาล็อก Commerce เพื่อระบุผลิตภัณฑ์ที่คุณต้องการนำเสนอในร้านค้าออนไลน์ B2B ของคุณ เมื่อคุณสร้างแค็ตตาล็อก คุณสามารถระบุร้านค้าออนไลน์ที่จะเสนอผลิตภัณฑ์ เพิ่มผลิตภัณฑ์ที่คุณต้องการรวม และเพิ่มข้อเสนอผลิตภัณฑ์โดยเพิ่มรายละเอียดการจัดซื้อสินค้า คุณสามารถสร้างแค็ตตาล็อกได้หลายแค็ตตาล็อกให้กับร้านค้าออนไลน์ B2B แต่ละร้าน ดังที่แสดงในภาพต่อไปนี้

![การแสดงตัวอย่างแค็ตตาล็อกผลิตภัณฑ์ของ Commerce](./media/Commerce_Catalogs.png)

แค็ตตาล็อกผลิตภัณฑ์ Commerce ให้คุณสามารถกําหนดข้อมูลต่อไปนี้:

- **ชนิดแค็ตตาล็อก** – ตั้งค่าคอนฟิกค่าเป็น **B2B** คุณสามารถกําหนดคุณสมบัติเฉพาะแค็ตตาล็อก B2B เช่น ลำดับชั้นการนำทาง ลำดับชั้นลูกค้า และข้อมูลเมตาของแอตทริบิวต์ของแค็ตตาล็อก 
- **ลำดับชั้นการนำทางเฉพาะแค็ตตาล็อก** – องค์กรสามารถสร้างโครงสร้างประเภทเฉพาะให้กับแค็ตตาล็อกเฉพาะได้
- **ข้อมูลเมตาของแอตทริบิวต์เฉพาะแค็ตตาล็อก** – แอตทริบิวต์มีรายละเอียดเกี่ยวกับผลิตภัณฑ์ โดยการกําหนดแอตทริบิวต์ให้กับประเภทของลำดับชั้นการนําทาง คุณสามารถกําหนดค่าให้กับแอตทริบิวต์เหล่านั้นที่ระดับของผลิตภัณฑ์ที่กําหนดให้กับประเภทนั้นได้ จากนั้นองค์กรสามารถทำงานเหล่านี้ให้เสร็จสิ้น:

    - ค่าแอตทริบิวต์เฉพาะแค็ตตาล็อก
    - ควบคุมการมองเห็นแอตทริบิวต์ในระดับแค็ตตาล็อก
    - เลือกตัวคัดสรรที่เฉพาะเจาะจงให้กับแค็ตตาล็อกแต่ละประเภท

- **ช่องทาง** – องค์กรสามารถเชื่อมโยงช่องทางออนไลน์ของ B2B มากกว่าหนึ่งช่องทางกับแค็ตตาล็อก การสนับสนุนแบบครบวงจรของแค็ตตาล็อกมีให้เฉพาะกับร้านค้าออนไลน์ B2B เท่านั้น
- **ลำดับชั้นของลูกค้า** – สำหรับช่องทาง B2B ที่กำหนด องค์กรสามารถสร้างแค็ตตาล็อกเฉพาะสำหรับคู่ค้า B2B ที่เลือกโดยเชื่อมโยงลำดับชั้นของลูกค้ากับแค็ตตาล็อกนั้น
- **กลุ่มราคา** – คุณสามารถตั้งค่าคอนฟิกราคาและโปรโมชันที่ระบุให้กับแค็ตตาล็อกที่กําหนด ความสามารถนี้เป็นเหตุผลหลักในการกำหนดแค็ตตาล็อกของช่องทาง B2B กลุ่มราคาสำหรับแค็ตตาล็อกช่วยให้องค์กรสามารถจัดหาผลิตภัณฑ์ให้กับองค์กร B2B ที่ต้องการ และใช้ราคาและส่วนลดที่ต้องการได้ ลูกค้า B2B ที่สั่งซื้อจากแค็ตตาล็อกที่ตั้งค่าคอนฟิกสามารถได้รับประโยชน์จากราคาพิเศษและโปรโมชันหลังจากที่พวกเขาลงชื่อเข้าใช้ไซต์ Commerce B2B เมื่อต้องการตั้งค่าคอนฟิกราคาเฉพาะของแค็ตตาล็อก เลือก **กลุ่มราคา** จากแท็บ **แค็ตตาล็อก** เพื่อเชื่อมโยงกลุ่มราคาหนึ่งกลุ่มขึ้นไปกับแค็ตตาล็อก ข้อตกลงทางค้า สมุดรายวันการปรับปรุงราคา และส่วนลดขั้นสูงทั้งหมดที่มีการเชื่อมโยงกับกลุ่มราคาเดียวกัน จะถูกนำไปใช้เมื่อลูกค้าสั่งจากแค็ตตาล็อกนั้น (ส่วนลดขั้นสูงรวมถึงค่าเกณฑ์ ปริมาณ และส่วนลดสำหรับการซื้อคละกัน) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกลุ่มราคา โปรดดูที่ [กลุ่มราคา](price-management.md#price-groups)

> [!NOTE]
> คุณลักษณะนี้พร้อมใช้งานตั้งแต่ Dynamics 365 Commerce รุ่น 10.0.27 เมื่อต้องการตั้งค่าคอนฟิกการตั้งค่าคอนฟิกเฉพาะแค็ตตาล็อก เช่น ลำดับชั้นการนำทางและลำดับชั้นลูกค้า ใน Commerce headquarters ไปที่พื้นที่ทำงาน **การจัดการคุณลักษณะ** (**การจัดการระบบ \> พื้นที่ทำงาน \> การจัดการคุณลักษณะ**) เปิดใช้งานคุณลักษณะ **เปิดใช้งานการใช้แค็ตตาล็อกหลายรายการในช่องทางการขายปลีก** แล้วเรียกใช้งาน **1110 CDX** เมื่อคุณเปิดใช้งานคุณลักษณะนี้ แค็ตตาล็อกทั้งหมดที่มีอยู่ที่ใช้กับร้านค้า POS หรือศูนย์บริการจะถูกเลือกเป็น **ชนิดของแค็ตตาล็อก = B2C** บนหน้า **แค็ตตาล็อก** เฉพาะแค็ตตาล็อกที่มีอยู่และแค็ตตาล็อกใหม่ที่มีการเครื่องหมายเป็น **ชนิดของแค็ตตาล็อก = B2C** เท่านั้นที่ใช้ได้กับร้านค้า POS และศูนย์บริการ 

## <a name="b2b-catalog-process-flow"></a>ผังลำดับกระบวนการของแค็ตตาล็อก B2B

กระบวนการในการสร้างและการจัดการแค็ตตาล็อกมีขั้นตอนทั่วไปสี่ขั้นตอน แต่ละขั้นตอนจะอธิบายโดยละเอียดในส่วนถัดไป

> [!NOTE]
> ก่อนที่คุณจะดําเนินการต่อ โปรดตรวจสอบให้แน่ใจว่าแค็ตตาล็อกมีการเครื่องหมายเป็น **ชนิดของแค็ตตาล็อก = B2B**

1. **[การตั้งค่าคอนฟิก](#configure-the-catalog)**

    - เชื่อมโยงลำดับชั้นการนำทาง
    - ระบุเวลามีผลบังคับใช้และวันหมดอายุ ถ้าเกี่ยวข้อง
    - เพิ่มและจัดประเภทผลิตภัณฑ์
    - เชื่อมโยงกลุ่มราคา
    - เชื่อมโยงลำดับชั้นของลูกค้าที่ใช้เฉพาะกับองค์กร B2B ของคุณ 
    - เชื่อมโยงกลุ่มแอตทริบิวต์มิติเริ่มต้นสำหรับตัวคัดสรร เช่น ขนาด ลักษณะ และสี
    - ตั้งค่าข้อมูลเมตาของแอตทริบิวต์

1. **[การตรวจสอบความถูกต้อง](#validate-the-catalog)** – ในขั้นตอนนี้ คุณเรียกใช้กฎการตรวจสอบความถูกต้องที่บังคับใช้ลักษณะการทำงานเฉพาะ ยกตัวอย่างเช่น

    - ตรวจสอบให้แน่ใจว่าไม่มีผลิตภัณฑ์ที่ไม่ได้จัดประเภท
    - ตรวจสอบให้แน่ใจว่าสินค้าทั้งหมดที่มีในประเภทแต่ละช่องทางเชื่อมโยงกับแค็ตตาล็อก

1. **[การอนุมัติ](#approve-the-catalog)**
1. **[กำลังเผยแพร่](#publish-the-catalog)**

## <a name="set-up-the-catalog"></a>ตั้งค่าแค็ตตาล็อก

ใช้ข้อมูลในส่วนนี้เพื่อตั้งค่าแค็ตตาล็อกของคุณ

### <a name="configure-the-catalog"></a>ตั้งค่าคอนฟิกแค็ตตาล็อก

ในศูนย์ควบคุม Commerce ให้ไปที่ **การขายปลีกและการค้า \> แค็ตตาล็อกและการจัดประเภท \> แค็ตตาล็อกทั้งหมด** เพื่อตั้งค่าคอนฟิกแค็ตตาล็อกของคุณ

เมื่อคุณสร้างแค็ตตาล็อกใหม่ อันดับแรกคุณต้องเชื่อมโยงแค็ตตาล็อกไปยังช่องทางอย่างน้อยหนึ่งช่องทาง เฉพาะสินค้าที่เชื่อมโยงกับ [การจัดประเภท](/dynamics365/unified-operations/retail/assortments) ของช่องทางที่คุณเลือกเท่านั้นที่สามารถใช้ได้ เมื่อสร้างแค็ตตาล็อก เมื่อต้องการเชื่อมโยงแค็ตตาล็อกกับช่องทางอย่างน้อยหนึ่งช่องทาง ให้เลือก **เพิ่ม** บนแท็บด่วน **ช่องทางการค้า** ของหน้า **การตั้งค่าแค็ตตาล็อก** โปรดตรวจสอบให้แน่ใจว่าแค็ตตาล็อกมีการเครื่องหมายเป็น **ชนิดของแค็ตตาล็อก = B2B**

#### <a name="associate-the-navigation-hierarchy"></a>เชื่อมโยงลำดับชั้นการนำทาง

เมื่อต้องการเพิ่มผลิตภัณฑ์ไปยังแค็ตตาล็อก คุณต้องเลือกลำดับชั้นการนำทาง ลำดับชั้นการนำทางสนับสนุนโครงสร้างประเภทสำหรับแค็ตตาล็อก คุณต้องเลือกจากหนึ่งในลำดับชั้นการนำทางที่เชื่อมโยงกับช่องทางที่คุณเลือกบนแท็บด่วน **ช่องทางการค้า** ของหน้า **การตั้งค่าแค็ตตาล็อก** เมื่อต้องการเชื่อมโยงลำดับชั้นการนําทางเริ่มต้นกับช่องทางแต่ละช่องทางของคุณ ให้ไปที่ **การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> ประเภทช่องทางและคุณลักษณะของผลิตภัณฑ์**

#### <a name="specify-time-effective-and-expiration-dates"></a>ระบุเวลาที่มีผลบังคับใช้และวันหมดอายุ

เมื่อต้องการระบุเวลาที่มีผลบังคับใช้เวลาและวันหมดอายุของแค็ตตาล็อก ให้เลือกโหนดบนสุดของแค็ตตาล็อกเพื่อกลับไปที่มุมมองส่วนหัวของแค็ตตาล็อกหลัก จากนั้นบนแท็บด่วน **ทั่วไป** ให้ตั้งค่าคอนฟิกวันที่มีผลบังคับใช้และวันหมดอายุตามความจำเป็น

#### <a name="add-and-categorize-products"></a>เพิ่มและจัดประเภทผลิตภัณฑ์

หากต้องการตั้งค่าคอนฟิกผลิตภัณฑ์เพื่อเพิ่มในแค็ตตาล็อก ในศูนย์ควบคุม Commerce ให้ไปที่ **การขายปลีกและการค้า \> แค็ตตาล็อกและการจัดประเภท \> แค็ตตาล็อกทั้งหมด** จากนั้นบนแท็บ **แค็ตตาล็อก** ให้เลือก **เพิ่มผลิตภัณฑ์**

หรือเลือกโหนดในลำดับชั้นการนำทาง จากนั้นคุณจะสามารถเพิ่มผลิตภัณฑ์ลงในประเภทในแค็ตตาล็อกโดยตรงได้

#### <a name="associate-price-groups"></a>เชื่อมโยงกลุ่มราคา

หากต้องการตั้งค่าคอนฟิกผลิตภัณฑ์เพื่อเพิ่มในแค็ตตาล็อก ในศูนย์ควบคุม Commerce ให้ไปที่ **การขายปลีกและการค้า \> แค็ตตาล็อกและการจัดประเภท \> แค็ตตาล็อกทั้งหมด** จากนั้นบนแท็บ **แค็ตตาล็อก** ให้เลือก **เพิ่มผลิตภัณฑ์** 

ผลิตภัณฑ์ที่เพิ่มในแค็ตตาล็อกจากโหนดรากของลำดับชั้นการนําทางโดยการเลือก **เพิ่มผลิตภัณฑ์** บนบานหน้าต่างการดำเนินการ จะสืบทอดประเภทของพวกเขา ถ้าลำดับชั้นการนําทางต้นทางเชื่อมโยงกับแค็ตตาล็อกด้วย การเปลี่ยนแปลงประเภทที่เกิดขึ้นบนลำดับชั้นการนําทางต้นทางจะสะท้อนให้เห็นในแค็ตตาล็อกในทันที คุณต้องเผยแพร่แค็ตตาล็อกใหม่เพื่ออัปเดตช่องทาง

อีกทางหนึ่งคือ คุณสามารถเลือกโหนดในลำดับชั้นการนำทางและเพิ่มผลิตภัณฑ์ลงในประเภทที่เลือกในแค็ตตาล็อกโดยตรง 

เมื่อคุณเพิ่มผลิตภัณฑ์ ตัวเลือก **รวมผลิตภัณฑ์ย่อยทั้งหมดโดยอัตโนมัติเมื่อเลือกผลิตภัณฑ์หลักเท่านั้น** จะพร้อมใช้งาน เมื่อต้องการป้องกันการรวมผลิตภัณฑ์ย่อยทั้งหมด ให้เลือกผลิตภัณฑ์หลักอย่างน้อยหนึ่งตัวแปร 

> [!NOTE]
> ถ้าคุณเลือกที่จะรวมผลิตภัณฑ์ย่อยทั้งหมดในการเลือกผลิตภัณฑ์หลักขนาดใหญ่โดยอัตโนมัติ คุณอาจประสบกับเวลาในการประมวลผลนานกว่า สำหรับการเลือกขนาดใหญ่ เราแนะนำให้คุณเลือก **รวมผลิตภัณฑ์ย่อยทั้งหมด** ในบานหน้าต่างการดําเนินการของหน้าแค็ตตาล็อกเพื่อรันการดําเนินงานในโหมดชุดงาน ถ้าคุณรวมเฉพาะผลิตภัณฑ์หลักในแค็ตตาล็อกและไม่ได้รวมผลิตภัณฑ์ย่อยใดๆ ตัวเลือกผลิตภัณฑ์ย่อยอาจไม่พร้อมใช้งานเมื่อคุณนําทางไปยังหน้ารายละเอียดผลิตภัณฑ์ 

เมื่อต้องการตั้งค่าคอนฟิกราคาเฉพาะแค็ตตาล็อก คุณต้องเชื่อมโยงกลุ่มราคาหนึ่งกลุ่มหรือมากกว่ากับแค็ตตาล็อก หากต้องการเชื่อมโยงกลุ่มราคากับแค็ตตาล็อก ในศูนย์ควบคุม Commerce ให้ไปที่ **การขายปลีกและการค้า \> แค็ตตาล็อกและการจัดประเภท \> แค็ตตาล็อกทั้งหมด** จากนั้นบนแท็บ **แค็ตตาล็อก** ภายใต้ **การกำหนดราคา** ให้เลือก **กลุ่มราคา** ข้อตกลงทางค้า สมุดรายวันการปรับปรุงราคา และส่วนลดขั้นสูงทั้งหมด (ขีดจำกัด ปริมาณ และส่วนลดสำหรับการซื้อคละกัน) ที่มีการเชื่อมโยงกับกลุ่มราคาเดียวกัน จะถูกนำไปใช้เมื่อลูกค้าสั่งจากแค็ตตาล็อก

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกลุ่มราคา ดูที่ [กลุ่มราคา](price-management.md#price-groups)

> [!NOTE]
> คุณไม่สามารถสร้างกลุ่มราคาใหม่จากหน้า **แค็ตตาล็อกทั้งหมด** คุณต้องสร้างกลุ่มราคาจากหน้า **กลุ่มราคาทั้งหมด** แทน จากนั้นคุณต้องเชื่อมโยงกับแค็ตตาล็อกในหน้า **แค็ตตาล็อกทั้งหมด**

#### <a name="associate-a-customer-hierarchy"></a>เชื่อมโยงลำดับชั้นของลูกค้า

หากต้องการเชื่อมโยงลำดับชั้นของลูกค้า ในศูนย์ควบคุม Commerce ให้ไปที่ **การขายปลีกและการค้า \> แค็ตตาล็อกและการจัดประเภท \> แค็ตตาล็อกทั้งหมด** จากนั้นบนแท็บ **แค็ตตาล็อก** ภายใต้ **ลำดับชั้นของลูกค้า** เลือก **กำหนดลำดับชั้น** เพื่อเชื่อมโยงลำดับชั้นของลูกค้าหนึ่งกับแค็ตตาล็อกอย่างน้อยหนึ่งลำดับ

> [!NOTE]
> คุณไม่สามารถสร้างลำดับชั้นของลูกค้าใหม่จากหน้า **แค็ตตาล็อกทั้งหมด** คุณต้องสร้างลำดับชั้นของลูกค้าจากหน้า **ลำดับชั้นของลูกค้า** แทน จากนั้นคุณต้องเชื่อมโยงกับแค็ตตาล็อกในหน้า **แค็ตตาล็อกทั้งหมด**

#### <a name="associate-default-dimension-attribute-group-for-refiners-such-as-size-style-and-color"></a>เชื่อมโยงกลุ่มแอตทริบิวต์มิติเริ่มต้นสำหรับตัวคัดสรร เช่น ขนาด ลักษณะ และสี

เมื่อต้องการเชื่อมโยงกลุ่มแอตทริบิวต์มิติเริ่มต้นสำหรับตัวคัดสรร เช่น ขนาด ลักษณะ และสี ในศูนย์ควบคุม Commerce ไปที่ **การขายปลีกและการค้า \> แค็ตตาล็อกและการจัดประเภท \> แค็ตตาล็อกทั้งหมด** จากนั้นบนแท็บ **แค็ตตาล็อก** ภายใต้ **คุณลักษณะ** ให้เลือก **กลุ่มคุณลักษณะ**

#### <a name="set-attribute-metadata"></a>ตั้งค่าข้อมูลเมตาของแอตทริบิวต์

หากต้องการตั้งค่าคอนฟิกข้อมูลเมตาของแอตทริบิวต์ ในศูนย์ควบคุม Commerce ให้ไปที่ **การขายปลีกและการค้า \> แค็ตตาล็อกและการจัดประเภท \> แค็ตตาล็อกทั้งหมด** จากนั้นบนแท็บ **แค็ตตาล็อก** ภายใต้ **คุณลักษณะ** ให้เลือก **ตั้งค่าข้อมูลเมตาของแอตทริบิวต์** เมื่อต้องการเลือกแอตทริบิวต์ที่ควรดูได้และปรับได้ ให้เลือกประเภทในลำดับชั้นการนําทางเฉพาะแค็ตตาล็อกที่เกี่ยวข้อง จากนั้นภายใต้ **คุณลักษณะของผลิตภัณฑ์ในแค็ตตาล็อก** ให้เลือกคุณลักษณะ จากนั้นเลือก **แสดงแอตทริบิวต์สำหรับช่องทาง** ตามค่าเริ่มต้น แอตทริบิวต์ที่ดูได้ทั้งหมดจะค้นหาได้ด้วย หากต้องการให้สามารถปรับปรุงคุณลักษณะได้ ให้เลือก **สามารถปรับได้**

### <a name="validate-the-catalog"></a>ตรวจสอบความถูกต้องของแค็ตตาล็อก

ก่อนที่แค็ตตาล็อกใหม่จะพร้อมใช้งาน จะต้องมีการตรวจสอบความถูกต้องและเผยแพร่

หากต้องการตรวจสอบแค็ตตาล็อก ทำตามขั้นตอนเหล่านี้

1. บนแท็บ **แค็ตตาล็อก** ของหน้า **แค็ตตาล็อกทั้งหมด** ภายใต้ **ตรวจสอบความถูกต้อง** เลือก **ตรวจสอบความถูกต้องของแค็ตตาล็อก** เพื่อเรียกใช้การตรวจสอบความถูกต้อง ขั้นตอนนี้มีความจำเป็น โดยจะตรวจสอบว่าการตั้งค่าที่จำเป็นนั้นถูกต้อง
1. เลือก **ดูผลลัพธ์** เพื่อดูรายละเอียดของการตรวจสอบความถูกต้อง ถ้าพบข้อผิดพลาด คุณต้องแก้ไขข้อมูล และเรียกใช้การตรวจสอบความถูกต้องอีกครั้งจนกว่าการตรวจสอบจะผ่าน

> [!NOTE]
> ถ้า **ชนิดแค็ตตาล็อก = B2B** การตรวจสอบความถูกต้องจะล้มเหลวถ้าคุณเพิ่มร้านค้า POS หรือศูนย์บริการในแค็ตตาล็อก แค็ตตาล็อก B2B ต้องมีการเชื่อมโยงช่องทางออนไลน์ B2B เท่านั้น การตรวจสอบความถูกต้องจะล้มเหลวด้วยหากไม่มีลำดับชั้นของลูกค้าที่เชื่อมโยงกับแค็ตตาล็อก B2B 

### <a name="approve-the-catalog"></a>อนุมัติแค็ตตาล็อก

หลังจากที่แค็ตตาล็อกผ่านการตรวจสอบความถูกต้อง จะต้องมีการอนุมัติ

การเริ่มต้นลำดับงานการอนุมัติแค็ตตาล็อก ให้ทำตามขั้นตอนเหล่านี้

1. ในบานหน้าต่างการดำเนินการของหน้า **แค็ตตาล็อกทั้งหมด** เลือก **ลำดับงาน \> ส่ง**
1. ไปที่ **การขายปลีกและการค้า \> การตั้งค่าศูนย์ควบคุม \> ลำดับงานการค้า** เพื่อตั้งค่าคอนฟิกขั้นตอนและผู้ใช้ที่ได้รับอนุญาตสำหรับลำดับงาน ลำดับงานจะกำหนดขั้นตอนต่างๆ ที่จำเป็นสำหรับการทำให้แค็ตตาล็อกอยู่ในสถานะ **อนุมัติแล้ว**

### <a name="publish-the-catalog"></a>เผยแพร่แค็ตตาล็อก

เมื่อแค็ตตาล็อกอยู่ในสถานะ **อนุมัติแล้ว** คุณสามารถเผยแพร่แค็ตตาล็อกได้โดยเลือก **เผยแพร่** ในเมนู **แค็ตตาล็อก** หลังจากแค็ตตาล็อกอยู่ในสถานะ **เผยแพร่แล้ว** จะสามารถใช้ในการป้อนข้อมูลใบสั่งศูนย์บริการ และส่งกระบวนการแค็ตตาล็อก คุณสามารถเผยแพร่แค็ตตาล็อกด้วยตนเองหรือใช้กระบวนการชุดงานก็ได้ วันที่มีผลบังคับใช้ที่คุณกําหนดไว้สำหรับแค็ตตาล็อกจะกําหนดว่าผลิตภัณฑ์มีอยู่ในร้านค้าออนไลน์เมื่อใด วันหมดอายุที่คุณกําหนดจะกําหนดว่าจะเอาผลิตภัณฑ์ออกจากร้านค้าออนไลน์เมื่อใด

> [!NOTE]
> คุณสามารถเผยแพร่แค็ตตาล็อกที่มีผลิตภัณฑ์ที่มีคําเตือนได้ อย่างไรก็ตาม ผลิตภัณฑ์เหล่านั้นจะไม่ปรากฏในร้านค้าออนไลน์

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ผลกระทบของความสามารถในการเพิ่มฟังก์ชันของแค็ตตาล็อก Commerce สำหรับการปรับแต่ง B2B](catalogs-b2b-sites-dev.md)

[คำถามที่ถามบ่อยเกี่ยวกับแค็ตตาล็อก Commerce สำหรับ B2B](catalogs-b2b-sites-FAQ.md)

[โมดูลตัวเลือกแค็ตตาล็อก](catalog-picker.md)
