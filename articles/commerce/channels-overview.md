---
title: ภาพรวมของช่องทาง
description: บทความนี้แสดงภาพรวมของช่องทางใน Microsoft Dynamics 365 Commerce
author: samjarawan
ms.date: 01/27/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: af5089f0065610873360b2e2883928a43600caa9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884648"
---
# <a name="channels-overview"></a>ภาพรวมของช่องทาง


[!include [banner](includes/banner.md)]

บทความนี้แสดงภาพรวมของช่องทางใน Microsoft Dynamics 365 Commerce โดยจะมีข้อมูลเกี่ยวกับภารกิจที่คุณต้องกรอกทั้งหมดก่อน และหลังจากที่คุณตั้งค่าแต่ละช่องทาง

## <a name="types-of-channels"></a>ชนิดของช่องทาง

Dynamics 365 Commerce รองรับช่องทางสามชนิดที่แตกต่างกัน ได้แก่ การขายปลีก ศูนย์บริการ และช่องทางออนไลน์

### <a name="retail-channels"></a>ช่องทางการขายปลีก

ช่องทางการขายปลีกแสดงถึงร้านค้าจริงมาตรฐาน ร้านค้าแต่ละร้านสามารถมีทะเบียนการขายหน้าร้าน (POS) ของตนเอง เงินได้ และบัญชีค่าใช้จ่าย และพนักงาน 

### <a name="call-center-channels"></a>ช่องทางศูนย์บริการ

ช่องทางของศูนย์บริการแสดงถึงใบสั่งศูนย์บริการ และการจัดการลูกค้า

### <a name="online-channels"></a>ช่องทางออนไลน์

ช่องทางออนไลน์แสดงถึงหน้าร้านพาณิชย์อิเล็กทรอนิกส์แบบออนไลน์ เมื่อมีการสร้างช่องทางออนไลน์ จะต้องสร้างไซต์โดยใช้โปรแกรมสร้างไซต์ Microsoft Microsoft Dynamics 365 Commerce หรือโซลูชันพาณิชย์อิเล็กทรอนิกส์อื่น ๆ ของบุคคลที่สาม

## <a name="channel-setup-basics"></a>ข้อมูลพื้นฐานเกี่ยวกับการตั้งค่าช่องทาง

การตั้งค่าช่องทางดำเนินการในเครื่องมือ Commerce แต่ละช่องทางสามารถมีวิธีการชำระเงินของตนเอง กลุ่มราคา ลำดับชั้นของผลิตภัณฑ์ การจัดประเภท และชุดของผลิตภัณฑ์ หลังจากที่คุณสร้างช่องทางแล้ว กำหนดผลิตภัณฑ์ที่คุณต้องการดำเนินการและขาย แต่ละชนิดของช่องทางมีชุดของลักษณะการทำงานเฉพาะที่อาจจำเป็นต้องได้รับการตั้งค่าคอนฟิก ตัวอย่างเช่น ช่องทางการขายปลีกจำเป็นต้องมีการกำหนดพนักงาน ทะเบียน และลูกค้า เมื่อสร้างช่องทางใหม่แล้ว ต้องกำหนดให้กับลำดับชั้นขององค์กรด้วย

## <a name="channel-setup-prerequisites"></a>ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง

ก่อนที่คุณจะสามารถตั้งค่าช่องทางได้ คุณต้องทำข้อกำหนดเบื้องต้นบางอย่างตามชนิดช่องทางให้เสร็จสมบูรณ์ สำหรับข้อมูลเพิ่มเติม ดูที่ [ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง](channels-prerequisites.md)

## <a name="set-up-a-channel"></a>ตั้งค่าช่องทาง

หลังจากที่คุณทำงานที่เป็นข้อกำหนดเบื้องต้นเสร็จสมบูรณ์แล้ว สำหรับคำแนะนำการตั้งค่าเพิ่มเติม ให้ใช้ลิงก์ต่อไปนี้

- [ตั้งค่าช่องทางการขายปลีก](channel-setup-retail.md)
- [ตั้งค่าช่องทางศูนย์บริการ](channel-setup-callcenter.md)
- [ตั้งค่าช่องทางออนไลน์](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง](channels-prerequisites.md)

[ตั้งค่าช่องทางการขายปลีก](channel-setup-retail.md)
    
[ตั้งค่าช่องทางออนไลน์](channel-setup-online.md)

[ตั้งค่าช่องทางศูนย์บริการ](channel-setup-callcenter.md)

[การตั้งค่าลำดับชั้นองค์กร](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]