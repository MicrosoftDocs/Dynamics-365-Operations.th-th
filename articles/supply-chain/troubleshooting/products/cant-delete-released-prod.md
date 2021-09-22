---
title: คุณไม่สามารถลบผลิตภัณฑ์ที่นำออกใช้ได้
description: คุณสามารถลบผลิตภัณฑ์ที่นำออกใช้และตัวแปรทั้งหมดได้เฉพาะเมื่อผลิตภัณฑ์ที่นำออกใช้ไม่มีธุรกรรมที่เกี่ยวข้องใด ๆ
author: SmithaNataraj
ms.date: 06/11/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f03d45a36401314a4b02ff354fabb474568c48b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477772"
---
# <a name="you-cant-delete-a-released-product"></a>คุณไม่สามารถลบผลิตภัณฑ์ที่นำออกใช้ได้

## <a name="symptoms"></a>อาการ

คุณสามารถลบผลิตภัณฑ์ที่นำออกใช้และตัวแปรทั้งหมดได้เฉพาะเมื่อผลิตภัณฑ์ที่นำออกใช้ไม่มีธุรกรรมที่เกี่ยวข้องใด ๆ

## <a name="resolution"></a>การแก้ปัญหา

ทำตามขั้นตอนต่อไปนี้เมื่อต้องการลบผลิตภัณฑ์หรือผลิตภัณฑ์หลักที่นำออกใช้

1. ปิดธุรกรรมที่เปิดค้างไว้ทั้งหมดสำหรับสินค้า
1. ลดสินค้าคงคลังเป็น 0 (ศูนย์)
1. ดำเนินการปิดสินค้าคงคลัง
1. ลบผลิตภัณฑ์ย่อยทั้งหมดสำหรับผลิตภัณฑ์หลักที่คุณต้องการลบออก
