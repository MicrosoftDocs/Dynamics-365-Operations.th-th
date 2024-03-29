---
title: การตั้งค่าผู้จัดจำหน่ายที่เพิ่มให้กับต้นทุนแฝง
description: บทความนี้จะอธิบายถึงฟิลด์ใหม่ที่จะเพิ่มเข้าในหน้าผู้จัดจำหน่ายที่มีอยู่ เมื่อคุณเปิดใช้งานโมดูลต้นทุนแฝง คุณใช้ฟิลด์เหล่านี้เพื่อตั้งค่าผู้จัดจำหน่ายที่คุณจะใช้ร่วมกับคุณลักษณะของต้นทุนแฝง
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 84d1dee0815b036a3d411eabff49d8a08249bed3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882589"
---
# <a name="vendor-settings-added-for-landed-cost"></a>การตั้งค่าผู้จัดจำหน่ายที่เพิ่มให้กับต้นทุนแฝง

[!include [banner](../../includes/banner.md)]

เมื่อคุณเปิดใช้งานโมดูล **ต้นทุนแฝง** ฟิลด์ใหม่จะเพิ่มเข้าในหน้า **ผู้จัดจำหน่าย** ที่มีอยู่ คุณใช้ฟิลด์เหล่านี้เพื่อตั้งค่าผู้จัดจำหน่ายที่คุณจะใช้ร่วมกับคุณลักษณะของต้นทุนแฝง

เมื่อต้องการตั้งค่าฟิลด์ที่เกี่ยวข้อง ให้ไปที่ **การจัดซื้อและการจัดหา \> ผู้จัดจำหน่าย \> ผู้จัดจำหน่ายทั้งหมด** เปิดผู้จัดจำหน่ายที่มีอยู่ หรือสร้างผู้จัดจำหน่ายใหม่ แล้วเลือกแท็บด่วน **รายละเอียดเบ็ดเตล็ด** ฟิลด์ใหม่ทั้งหมดที่โมดูล **ต้นทุนแฝง** เพิ่มจะปรากฏขึ้นภายใต้หัวข้อ **การเดินทาง** ตารางต่อไปนี้อธิบายฟิลด์เหล่านี้

| ฟิลด์ | คำอธิบาย |
|---|---|
| ชนิดการจัดส่ง | <p>เลือกบทบาทของผู้จัดจำหน่ายที่เกี่ยวข้องกับต้นทุนแฝง:</p><ul><li>**ไม่มี** – ผู้จัดจำหน่ายไม่มีบทบาทเฉพาะที่เกี่ยวข้องกับต้นทุนแฝง ค่านี้เป็นการตั้งค่าเริ่มต้น เนื่องจากผู้จัดจำหน่ายส่วนใหญ่จะไม่มีบทบาทเฉพาะ</li><li>**บริษัทผู้จัดส่ง** – ผู้จัดจำหน่ายเป็นบริษัทขนส่ง ผู้จัดจำหน่ายที่มีชนิดการจัดส่งนี้พร้อมใช้งานเฉพาะเมื่อเลือกในฟิลด์ **บริษัทการจัดส่ง** ในหน้า **การเดินทาง**</li><li>**นายหน้าศุลกากร** – ผู้จัดจำหน่ายเป็นนายหน้าศุลกากร ผู้จัดจำหน่ายที่มีชนิดการจัดส่งนี้พร้อมใช้งานเฉพาะเมื่อเลือกในฟิลด์ **นายหน้าศุลกากร** ในหน้า **ใบแจ้งรายการ**</li><li>**ตัวแทน** – ผู้จัดจำหน่ายเป็นตัวแทน ผู้จัดจำหน่ายที่มีชนิดการจัดส่งนี้พร้อมใช้งานเฉพาะเมื่อเลือกในฟิลด์ **ตัวแทน** ในหน้า **ผู้จัดจำหน่าย** และ **ใบสั่งซื้อ**</li></ul> |
| กลุ่มชนิดต้นทุน | กําหนดผู้จัดจำหน่ายให้กับกลุ่มชนิดต้นทุน เพื่อวัตถุประสงค์ในการเลือก [ต้นทุนอัตโนมัติ](auto-cost-setup.md) |
| จากท่าเรือ | เลือกท่าเรือผู้ผลิตสำหรับการเดินทาง |
| ตัวแทน | ตัวแทนเริ่มต้นเมื่อจัดซื้อจากผู้จัดจำหน่าย |
| นำเข้าผู้จัดจำหน่ายการคิดต้นทุน | <p>บ่งชี้ว่าผู้จัดจำหน่ายเป็นผู้จัดจำหน่ายต้นทุนแฝงหรือไม่</p><p>**คำแนะนำ:** คุณสามารถใช้ฟิลด์นี้ร่วมกับความปลอดภัยระดับเรกคอร์ดเพื่อจํากัดใบสั่งซื้อที่แสดงเมื่อสร้างการเดินทาง</p> |
| บริษัทจัดส่งสินค้า | เลือกบริษัทที่จัดส่งเริ่มต้นที่จะใช้เมื่อสร้างใบสั่งซื้อส้รับให้แก่ผู้จัดจำหน่าย |
| ผู้ให้บริการ | บ่งชี้ว่าผู้จัดจำหน่ายเป็นผู้ให้บริการหรือไม่ |
| กลุ่มการยอมรับมาก/น้อยเกินไป | เลือกกลุ่มการยอมรับมากเกิน/ต่ำกว่าค่าเริ่มต้นสำหรับผู้จัดจำหน่าย |
