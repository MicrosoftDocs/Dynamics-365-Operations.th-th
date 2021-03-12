---
title: เพิ่มสถานที่และชนิดความสัมพันธ์ของฝ่าย
description: หัวข้อนี้อธิบายวิธีการเพิ่มสถานที่ใหม่และชนิดความสัมพันธ์ของฝ่าย
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 00810576d36339bf7ce0657b1577e1e322c36bf0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979100"
---
# <a name="add-location-and-party-relationship-types"></a>เพิ่มสถานที่และชนิดความสัมพันธ์ของฝ่าย 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a>เพิ่มบทบาทสถานที่

มีวิธีสองวิธีที่จะเพิ่มบทบาทสถานที่ใหม่สำหรับที่อยู่และข้อมูลผู้ติดต่อ:

-  เพิ่มผ่านทางหน้า **วัตถุประสงค์ของที่อยู่และข้อมูลการติดต่อ** บทบาทใหม่จะถูกบันทึกไปยังตาราง **LogisticsLocationRole** ที่มีชนิด = 0 ซึ่งบ่งชี้ว่า บทบาทไม่ใช่บทบาทของระบบที่กำหนดไว้ใน enum **LogisticsLocationRoleType** และส่วนขยาย ผู้ใช้จะสามารถใช้บทบาทนี้ได้ เมื่อสร้างข้อมูลที่อยู่หรือผู้ติดต่อ

    ![วัตถุประสงค์ของที่อยู่และข้อมูลผู้ติดต่อ](media/Address-Contact.PNG)

-  เพิ่มเข้าไปยังส่วนขยาย enum **LogisticsLocationRoleType** และปล่อยให้โปรแกรมเติมข้อมูลผ่านกระบวนการซิงค์ฐานข้อมูล

    1.  สร้างการขยายไปยัง enum **LogisticsLocationRoleType** และเพิ่มบทบาทใหม่ในส่วนขยาย 
  
        ![ส่วนขยายไปยังการแจงนับ LogisticsLocationRoleType](media/Logistics.PNG)

    2. สร้างไฟล์ทรัพยากรใหม่สำหรับบทบาทใหม่ และจากนั้น กำหนดค่าสำหรับคุณสมบัติ
     
     ![ไฟล์ทรัพยากรใหม่](media/Resource.PNG)
        
    3.  สร้างคลาสการเติมข้อมูล และให้วิธีการจัดการเพื่อเติมข้อมูลบทบาทใหม่ 

        ![การเติมข้อมูล](media/Dirdata.PNG)

    4.  เพื่อทดสอบการนำเข้าข้อมูลบทบาทสถานที่ใหม่ คุณสามารถสร้างคลาสที่สามารถรันได้ และเรียกใช้ DirDataPopulation::insertLogisticsLocationRoles() ใน Main() หลังจากกระบวนการนี้เสร็จสมบูรณ์ คุณควรเห็นบทบาทใหม่ที่เติมข้อมูลในตาราง **LogisticsLocationRole** ที่มีชนิด \> 0 บทบาทใหม่จะแสดงบนหน้า **วัตถุประสงค์ของที่อยู่และข้อมูลผู้ติดต่อ**

        ![แทรกสถานที่ใหม่](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a>เพิ่มชนิดความสัมพันธ์ของฝ่าย 

มีวิธีสองวิธีในการเพิ่มชนิดความสัมพันธ์ใหม่:

-   เพิ่มผ่านหน้า **ชนิดของความสัมพันธ์** ความสัมพันธ์ใหม่จะถูกบันทึกลงใน **DirRelationshipTypeTable** ที่มี systemtype = 0

    ![ชนิดของความสัมพันธ์](media/Relationship.PNG)

-  เพิ่มเข้าไปยังส่วนขยายของ enum **DirSystemRelationshipType** และปล่อยให้โปรแกรมเติมข้อมูลผ่านกระบวนการซิงค์ฐานข้อมูล

    1.  สร้างการขยายไปยัง enum **DirSystemRelationshipType** และเพิ่มชนิดความสัมพันธ์ใหม่

    2. สร้างตัวเริ่มต้นสำหรับชนิดใหม่นี้ คุณสามารถค้นหาตัวอย่างที่หลากหลายในรหัสหลัก หนึ่งในนั้นคือ  **DirRelationshipTypeChildInitialize** นี่คือคลาสตัวเริ่มต้นสำหรับชนิดความสัมพันธ์ของฝ่าย "รอง" คุณสามารถเริ่มต้นด้วยตัวเริ่มต้นของคุณโดยการคัดลอกและการวางรหัสนี้ และจากนั้น อัพเดตพื้นที่ที่เน้น
    
    ![ตัวเริ่มต้น DirRelationshipChild](media/DirRelationship.PNG)

    3.  เพื่อทดสอบการนำเข้าข้อมูลชนิดความสัมพันธ์ใหม่ คุณสามารถสร้างคลาสที่สามารถรันได้ และเรียกใช้ DirDataPopulation::insertDirRelationshipTypes() ใน Main() คุณควรเห็นชนิดความสัมพันธ์ใหม่ใน **DirRelationshipTypeTable** และชนิดความสัมพันธ์ใหม่จะพร้อมใช้งานบนหน้า **ชนิดของความสัมพันธ์**

        ![คลาสที่สามารถรันได้](media/Runnable.PNG)
