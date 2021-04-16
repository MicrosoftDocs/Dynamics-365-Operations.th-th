---
title: การแก้ไขปัญหาการเติมสินค้าในคลังสินค้า
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการเติมสินค้าในคลังสินค้าใน Microsoft Dynamics 365 Supply Chain Management
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8940f729e1115405e8d6e50eccc92d9fffe37f3e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828093"
---
# <a name="troubleshoot-warehouse-replenishment"></a>การแก้ไขปัญหาการเติมสินค้าในคลังสินค้า

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการเติมสินค้าในคลังสินค้าใน Microsoft Dynamics 365 Supply Chain Management

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a>ฉันการเติมสินค้าได้รับข้อความข้อผิดพลาดต่อไปนี้: "งาน %1 ไม่สามารถปลดบล็อคได้ เนื่องจากมีงานการเติมสินค้าที่ยังไม่เสร็จสิ้น"

### <a name="issue-description"></a>คำอธิบายปัญหา

งานการเบิกสินค้าถูกบล็อคเนื่องจากงานการเติมสินค้าที่มีการเชื่อมโยง

### <a name="issue-resolution"></a>การแก้ไขปัญหา

เมื่อคุณใช้การเติมสินค้าตามความต้องการของเวฟ ถ้าต้องเติมสถานที่เบิกสินค้าเพื่อตอบสนองความต้องการของใบสั่งต้นทาง ระบบจะสร้างทั้งงานการเติมสินค้าและงานการเบิกสินค้า อย่างไรก็ตาม จะบล็อคงานการเบิกสินค้าจนกว่างานการเติมสินค้าจะเสร็จสมบูรณ์ ลักษณะการทำงานนี้มีเจตนา เนื่องจากสถานที่เบิกสินค้าจะไม่มีสินค้าคงคลังเพียงพอยกเว้นว่างานการเติมสินค้าเสร็จสมบูรณ์แล้ว ทำงานการเติมสินค้าให้เสร็จสมบูรณ์ แล้วประมวลผลงานการเบิกสินค้า


[!INCLUDE[footer-include](../../includes/footer-banner.md)]