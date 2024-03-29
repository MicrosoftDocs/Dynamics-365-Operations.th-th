---
title: การตั้งค่าผู้จัดจำหน่าย ลูกค้า และสินค้าสำหรับการค้าระหว่างบริษัท
description: บทความนี้จะอธิบายถึงวิธีการตั้งค่าผู้จัดจำหน่าย ลูกค้า และสินค้าสำหรับการค้าระหว่างบริษัท
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4c928435a4e66832b09dbc805664934cfb1236be
ms.sourcegitcommit: b666289f5113d0a3fa2220fe337d5aacf07cbd92
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/08/2022
ms.locfileid: "8945768"
---
# <a name="set-up-vendors-customers-and-items-for-intercompany-trade"></a>การตั้งค่าผู้จัดจำหน่าย ลูกค้า และสินค้าสำหรับการค้าระหว่างบริษัท

[!include [banner](../../includes/banner.md)]

หากต้องการจัดเตรียมองค์กรของคุณให้พร้อมรับการค้าระหว่างบริษัท คุณต้องกําหนดผู้จัดจำหน่ายและลูกค้าที่คุณจะทำการค้าภายใน จากนั้นคุณต้องเชื่อมโยงผู้จัดจำหน่ายและลูกค้าเหล่านี้กับสินค้าที่คุณจะซื้อหรือขาย

1. ไปที่ **การจัดซื้อและการจัดหา \> ผู้จัดจำหน่าย \> ผู้จัดจำหน่ายทั้งหมด**
1. เลือกผู้จัดจำหน่ายเพื่อกําหนดเป็นผู้จัดจำหน่ายระหว่างบริษัท
1. บนบานหน้าต่างการดำเนินการ บนแท็บ **ทั่วไป** เลือก **ระหว่างบริษัท**
1. ระบุพารามิเตอร์การตั้งค่าระหว่างบริษัทสำหรับบัญชีผู้จัดจำหน่าย พารามิเตอร์เหล่านี้รวมถึงนิติบุคคลและบัญชีของลูกค้า นโยบายใบสั่งขาย นโยบายใบสั่งซื้อ การแม็ปค่า และข้อตกลงการซื้อ และนโยบายข้อตกลงการขาย คุณยังระบุว่าจะใช้ค่าข้อมูลพื้นฐานจากบัญชีผู้จัดจำหน่ายหรือจากบัญชีลูกค้าในนิติบุคคลอื่นๆ
1. ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**
1. บนหน้ารายการ **ผลิตภัณฑ์ที่นำออกใช้** ให้เลือกสินค้าที่จะกําหนดให้กับผู้จัดจำหน่าย เพื่อให้สินค้านั้นพร้อมใช้งานได้สำหรับการค้าระหว่างบริษัท สำหรับสินค้าแต่ละรายการ เปิดหน้า **รายละเอียดผลิตภัณฑ์ที่นำออกใช้** บนแท็บ **ซื้อ** ในฟิลด์ **ผู้จัดจำหน่าย** ให้พิมพ์หมายเลขผู้จัดจำหน่าย
1. ไปที่ **บัญชีลูกหนี้ \> ลูกค้า \> ลูกค้าทั้งหมด**
1. เลือกลูกค้าเพื่อกําหนดเป็นลูกค้าระหว่างบริษัท
1. บนบานหน้าต่างการดำเนินการ บนแท็บ **ทั่วไป** เลือก **ระหว่างบริษัท**
1. ระบุพารามิเตอร์การตั้งค่าระหว่างบริษัทสำหรับบัญชีลูกค้า พารามิเตอร์เหล่านี้รวมถึงนิติบุคคลและบัญชีของผู้จัดจำหน่าย นโยบายใบสั่งซื้อ นโยบายใบสั่งขาย การแม็ปค่า และข้อตกลงการขาย และนโยบายข้อตกลงการซื้อ คุณยังระบุว่าจะใช้ค่าข้อมูลพื้นฐานจากบัญชีลูกค้าหรือจากบัญชีผู้จัดจำหน่ายในนิติบุคคลอื่นๆ
1. เมื่อคุณตั้งค่าพารามิเตอร์ระหว่างบริษัทเสร็จแล้ว ให้ปิดหน้า **ระหว่างบริษัท** เพื่อกลับไปที่รายละเอียดลูกค้าที่เลือก
1. ขยายแท็บด่วน **รายละเอียดเบ็ดเตล็ด** และตั้งค่า **สร้างใบสั่งระหว่างบริษัท** เป็น *ใช่* ถ้าคุณยังต้องการจัดส่งสินค้าตามใบสั่งให้กับลูกค้าโดยตรง ให้ตั้งค่า **การจัดส่งสินค้าโดยตรง** เป็น *ใช่*

    > [!NOTE]
    > ถ้ามีสินค้าบางรายการที่องค์กรของคุณเก็บสต็อกไว้และจัดส่งไปให้ลูกค้า คุณอาจไม่ต้องการสร้างใบสั่งระหว่างบริษัทโดยอัตโนมัติ แม้กระทั่งเมื่อคุณมีสินค้าอยู่ในสต็อก ถ้าต้องการปิดใช้งานการสร้างใบสั่งโดยอัตโนมัติ สำหรับสินค้าที่คุณอาจมีอยู่ในสต็อก ตั้งค่า **สร้างใบสั่งระหว่างบริษัท** เป็น *ไม่*

1. ถ้าคุณต้องการอนุญาตให้มีการสร้างบรรทัดเพิ่มเติมโดยอ้อมบนใบสั่งขาย ตั้งค่า **สร้างรายการใบสั่งทางอ้อม** เป็น *ใช่* จากนั้นผู้ใช้สามารถเพิ่มบรรทัดให้กับต้นฉบับใบสั่งขายจากใบสั่งขายระหว่างบริษัทได้

> [!WARNING]
> ถ้าคุณอนุญาตให้มีการสร้างบรรทัดใบสั่งโดยอ้อมได้ เท่ากับว่าคุณอนุญาตให้สามารถเพิ่มรายการทั้งหมดในต้นฉบับใบสั่งขายจากใบสั่งขายระหว่างบริษัทได้ จากนั้นการเพิ่มแต่ละครั้งจะมีการประมวลผลผ่านไปยังลูกค้า และเพิ่มเข้าในใบสั่งและใบแจ้งหนี้ นอกจากนี้ เอกสารทุกฉบับที่เกี่ยวข้องในการขายจะถูกพิมพ์และลงรายการบัญชีโดยอัตโนมัติ ผู้ใช้ไม่ได้รับการแจ้งเตือนเกี่ยวกับการเพิ่ม

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
