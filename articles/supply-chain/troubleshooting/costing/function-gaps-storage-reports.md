---
title: ช่องว่างระหว่างมูลค่าสินค้าคงคลัง/รายงานอายุหนี้และรุ่นการจัดเก็บ
description: ช่องว่างระหว่างมูลค่าสินค้าคงคลัง/รายงานอายุหนี้และรุ่นการจัดเก็บ
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a72e2d32e755e137cebbc0bf7afb0bed08fb93f2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477764"
---
# <a name="functional-gaps-between-inventory-valueaging-reports-and-their-storage-versions"></a>ช่องว่างระหว่างมูลค่าสินค้าคงคลัง/รายงานอายุหนี้และรุ่นการจัดเก็บ

ลักษณะการทำงาน [การจัดเก็บรายงานการแยกอายุสินค้าคงคลัง](/dynamics365/supply-chain/cost-management/inventory-aging-report-storage.md) และ [รายงานการจัดเก็บค่าสินค้าคงคลัง](/dynamics365/supply-chain/cost-management/inventory-value-report-storage.md) จะเปิดใช้งาน Supply Chain Management เพื่อแสดงปริมาณขนาดใหญ่ของธุรกรรมสินค้าคงคลัง ในแต่ละกรณี ผลลัพธ์ของรายงานจะถูกบันทึกไว้สำหรับการเรียกดูและการส่งออก ซึ่งแตกต่างจากรุ่นที่ไม่มีการจัดเก็บของรายงานเหล่านี้ อย่างไรก็ตาม ฟังก์ชันบางอย่างที่มีอยู่ในรุ่นที่ไม่มีการจัดเก็บรายงานเหล่านี้ไม่มีอยู่ในรุ่นการจัดเก็บ ย่อยต่อไปนี้สรุปความแตกต่างและให้การแก้ไขปัญหา

## <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>รายงานการจัดเก็บไม่มีผลรวมย่อยถึง แม้ว่าจะมีการเปิดใช้งานในโครงร่างรายงานหรือไม่

ผลรวมย่อยอาจทำให้เกิดปัญหาเมื่อส่งออกผลลัพธ์ โดยเฉพาะถ้าผู้ใช้เปลี่ยนลำดับเรกคอร์ด

เมื่อต้องการตรวจสอบผลรวมย่อย คุณสามารถส่งออกผลลัพธ์ไปยัง Microsoft Excel ได้ อีกทางหนึ่งคือ ถ้าคุณต้องการตรวจสอบผลรวมย่อยภายใน Supply Chain Management ให้ใช้ [การจัดการคุณลักษณะ](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อเปิดใช้งาน *ตัวควบคุมกริดใหม่* และคุณลักษณะ *การจัดกลุ่มในกริด* ซึ่งช่วยให้คุณสามารถดูผลรวมย่อยของกลุ่มใดก็ได้ตามต้องการ สำหรับข้อมูลเพิ่มเติม โปรดดูที่: [ความสามารถของกริด](/dynamics365/fin-ops-core/fin-ops/get-started/grid-capabilities.md)

## <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>รายงานการจัดเก็บมูลค่าสินค้าคงคลังไม่สนับสนุนข้อมูลบัญชีแยกประเภท

คุณสามารถรันงบทดลองเพื่อเรียกดูยอดดุลบัญชีสินค้าคงคลังและเปรียบเทียบกับรายงาน **ที่จัดเก็บค่าสินค้าคงคลัง** ได้
