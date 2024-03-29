---
title: กลยุทธ์การเติมสินค้า
description: บทความนี้จะนำเสนอข้อมูลเกี่ยวกับกลยุทธ์การเติมสินค้า และอธิบายวิธีการที่คุณสามารถใช้ฟิลด์กลยุทธ์การเติมสินค้าบนบรรทัดแม่แบบการเพิ่มเติมสินค้าตามความต้องการของเวฟเพื่อเลือกวิธีการเติมสินค้าที่ทำ
author: Mirzaab
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-29
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 1245d07436a9b57ee4f0402687e7a4367668cbfa
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336289"
---
# <a name="replenishment-strategies"></a>กลยุทธ์การเติมสินค้า

[!include [banner](../includes/banner.md)]

แม่แบบที่กำหนดบนหน้า **แม่แบบการเติมสินค้า** รวมถึงบรรทัดแม่แบบการเติมสินค้าตามความต้องการของเวฟซึ่งช่วยให้คุณสามารถเลือกว่าจะทำการเพิ่มเติมสินค้าอย่างไร แต่ละบรรทัดมีฟิลด์ **กลยุทธ์การเติมสินค้า**

กลยุทธ์ *ปริมาณความต้องการของเวฟ* เป็นกลยุทธ์เริ่มต้น กลยุทธ์การเติมสินค้าที่ใช้อยู่ก่อนการแนะนำของฟิลด์ **กลยุทธ์การเติมสินค้า** ใช้คำสั่งสถานที่การเติมสินค้าเพื่อค้นหาสถานที่ที่สามารถเติมสินค้าได้ จากนั้นจะเติมสินค้าที่ตั้งดังกล่าวจนครอบคลุมความต้องการ

กลยุทธ์ *ความจุของสถานที่เก็บสูงสุด* แนะนำฟังก์ชันใหม่ ๆ บางอย่าง เช่นเดียวกับกลยุทธ์ *ปริมาณความต้องการของเวฟ* กลยุทธ์นี้ใช้คำสั่งสถานที่สำหรับการเติมสินค้าเพื่อค้นหาสถานที่ที่สามารถเติมสินค้าได้ แล้วจึงเติมสินค้าที่ตั้งเหล่านั้นจนครอบคลุมความต้องการ ซึ่งแตกต่างจากกลยุทธ์ *ปริมาณความต้องการของเวฟ* ในสถานที่ที่เติมทั้งหมดจะถูกเติมไปยังกำลังการผลิตสูงสุด ตามที่กำหนดโดยขีดจำกัดของสถานที่เก็บ กลยุทธ์ *ความจุของสถานที่เก็บสูงสุด* พยายามสร้างงานเพื่อนำมาในปริมาณที่ร้องขอ บวกด้วยปริมาณพิเศษบางอย่าง เพื่อเติมสถานที่ที่มีการเติมสินค้า อย่างไรก็ตาม ในบางกรณีความพยายามดังกล่าวอาจล้มเหลว ตัวอย่างเช่น สถานที่เก็บสินค้าจำนวนมากอาจมีสินค้าคงคลังไม่เพียงพอที่จะครอบคลุมปริมาณพิเศษ ในกรณีเหล่านี้ ระบบตรวจพบความล้มเหลวและพยายามกู้คืน

พีคซีซั่นเป็นตัวอย่างหนึ่งของสถานการณ์ที่กลยุทธ์ *ความจุของสถานที่เก็บสูงสุด* สามารถใช้ได้กับกลยุทธ์ *ปริมาณความต้องการของเวฟ* ในช่วงพีคซีซั่น สินค้าบางรายการอาจมีการขายที่ปริมาณสูง ดังนั้น คุณอาจต้องการเติมสินค้าให้สถานที่เบิกสินค้าที่เกี่ยวข้องให้มากที่สุดเท่าที่จะเป็นไปได้เพื่อลดจำนวนของรหัสงานที่สร้างขึ้นสำหรับการเติมสินค้า

> [!IMPORTANT]
> เมื่อต้องการใช้ประโยชน์แบบเต็มของกลยุทธ์ *ความจุของสถานที่เก็บสูงสุด* คุณต้องกำหนดขีดจำกัดของการเก็บสต็อกสินค้าใหม่สำหรับสถานที่เก็บที่เกี่ยวข้อง มิฉะนั้น กลยุทธ์นี้ทำงานเช่นเดียวกับกลยุทธ์ *ปริมาณความต้องการของเวฟ*

## <a name="turn-on-the-replenish-to-max-based-on-stocking-limits-feature"></a>เปิดใช้งานคุณลักษณะเติมสินค้าจนสูงสุดตามขีดจำกัดสูงสุด

ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดคุณลักษณะนี้ในระบบของคุณก่อน ผู้ดูแลระบบสามารถใช้พื้นที่ทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งาน หากจำเป็น มีคุณลักษณะที่แสดงอยู่ในลักษณะต่อไปนี้:

- **โมดูล:** *การจัดการคลังสินค้า*
- **ชื่อคุณลักษณะ:** *เปิดใช้งานคุณลักษณะเติมสินค้าจนสูงสุดตามขีดจำกัดสูงสุด*

## <a name="set-up-replenishment-strategies"></a>ตั้งค่ากลยุทธ์การเติมสินค้า

หากต้องการเข้าถึงแม่แบบ ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การเติมสินค้า \> แม่แบบการเติมสินค้า** ในส่วน **ภาพรวม** ให้เลือกหรือสร้างแม่แบบการเติมสินค้าตามความต้องการของเวฟ ซึ่งฟิลด์ **ชนิดการเติมสินค้า** ถูกตั้งค่าเป็น *ความต้องการของเวฟ* ตั้งค่าบรรทัดแม่แบบการเติมสินค้าในส่วน **รายละเอียดแม่แบบการเติมสินค้า** สำหรับแต่ละบรรทัดในฟิลด์ **กลยุทธ์การเติมสินค้า** ให้เลือกกลยุทธ์การเติมสินค้าที่คุณต้องการใช้

![หน้าเท็มเพลตการเติมสินค้า](media/ReplenTempWaveDmdMaxLocCap.png "หน้าแม่แบบการเติมสินค้า")

ถ้าคอลัมน์ **กลยุทธ์การเติมสินค้า** ไม่ปรากฏในกริดในส่วน **รายละเอียดแม่แบบการเติมสินค้า** ตรวจสอบให้แน่ใจว่ามีการเปิดใช้งานลักษณะการทำงานแล้ว และแม่แบบการเติมสินค้าที่เลือกมีชนิดการเติมของ *ความต้องการของเวฟ*

> [!NOTE]
> กลยุทธ์ *ปริมาณความต้องการของเวฟ* เป็นกลยุทธ์เริ่มต้น อย่างไรก็ตาม คุณต้องอัพเดตรายการแม่แบบการเติมสินค้าที่คุณต้องการใช้กลยุทธ์ *ความจุของสถานที่เก็บสูงสุด* แทน

## <a name="example-scenarios"></a>สถานการณ์จำลองตัวอย่าง

### <a name="example-1"></a>ตัวอย่างที่ 1

สำหรับตัวอย่างนี้ มีแม่แบบการเติมสินค้าเพียงรายการเดียวที่มีบรรทัดแม่แบบการเติมสินค้าเพียงรายการเดียวเท่านั้น

คุณสร้างใบสั่งขายสำหรับ 130 ชิ้น (pcs) ของสินค้า A0001 ก่อนที่คุณจะนำใบสั่งออกใช้ไปยังคลังสินค้า คลังสินค้าจะถูกตั้งค่าในลักษณะต่อไปนี้

- มีสถานที่เก็บสินค้าจำนวนมากเพียงแห่งเดียวเท่านั้น และมี 500 ชิ้นของปริมาณคงคลังคงเหลือที่พร้อมใช้งาน
- มีสถานที่เบิกสินค้าสามแห่งซึ่งแต่ละแห่งมีขีดจำกัดของการเก็บสต็อกของ 100 ชิ้น (โปรดจำไว้ว่าจำเป็นต้องมีขีดจำกัดการเก็บสต็อกสำหรับกลยุทธ์ *ความจุสูงสุดของสถานที่เก็บ*)
- สถานที่การสำรองสินค้าสำหรับการเติมสินค้าจะเหมือนกับสถานที่เบิกสินค้าขาย
- หน่วยการเติมสินค้าเป็นกล่อง (1 กล่อง = 20 ชิ้น)

ในขณะใบสั่ง สินค้าคงคลังต่อไปนี้จะอยู่ในปริมาณคงคลังคงเหลือในสถานที่เบิกสินค้าขาย:

- **การเบิกสินค้า-001:** 20 ชิ้น (1 กล่อง)
- **การเบิกสินค้า-002:** 0 ชิ้น
- **การเบิกสินค้า-003:** 0 ชิ้น

ในขั้นต้น กลยุทธ์การเติมสินค้าจะถูกตั้งค่าเป็น *ปริมาณความต้องการของเวฟ*

หลังจากที่คุณนำใบสั่งขายออกใช้ไปยังคลังสินค้า และการประมวลผลเวฟรันสำหรับเวฟ คุณจะได้รับงานการเติมสินค้าดังต่อไปนี้

- **งานการเพิ่มเติมสินค้า 1:** เบิกสินค้า 4 กล่องจากสถานที่เก็บสินค้าจำนวนมากและใส่ไว้ในสถานที่เบิกสินค้า-001
- **งานการเพิ่มเติมสินค้า 2:** เบิกสินค้า 2 กล่องจากสถานที่เก็บสินค้าจำนวนมากและใส่ไว้ในสถานที่เบิกสินค้า-002

คุณจะได้รับรหัสงานการเติมสินค้าสองรหัส เนื่องจากคุณต้องเติมสินค้าสองแห่งและไม่ได้รับการสนับสนุนหลายตำแหน่ง

ถ้าคุณกำหนดกลยุทธ์การเติมสินค้าเป็น *ความจุของสถานที่เก็บสูงสุด* แทน คุณจะได้รับงานการเติมสินค้าต่อไปนี้:

- **งานการเพิ่มเติมสินค้า 1:** เบิกสินค้า 4 กล่องจากสถานที่เก็บสินค้าจำนวนมากและใส่ไว้ในสถานที่เบิกสินค้า-001
- **งานการเพิ่มเติมสินค้า 2:** เบิกสินค้า 5 กล่องจากสถานที่เก็บสินค้าจำนวนมากและใส่ไว้ในสถานที่เบิกสินค้า-002

[![ตัวอย่าง 1](media/ReplenTemp_example_1.png "ตัวอย่างที่ 1")](media/ReplenTemp_example_1_large.png)

### <a name="example-2"></a>ตัวอย่างที่ 2

ตัวอย่างนี้แสดงให้เห็นว่าเกิดอะไรขึ้นเมื่อสถานที่เก็บสินค้าจำนวนมากมีสินค้าคงคลังไม่เพียงพอที่จะครอบคลุมปริมาณพิเศษ ใช้สถานการณ์จำลองเดียวกันกับตัวอย่างที่ 1 แต่ที่ตั้งจำนวนมากมี 160 ชิ้น (กล่อง 8)

กลยุทธ์ *ปริมาณความต้องการของเวฟ* สร้างงานเดียวกันกับที่มีอยู่ในตัวอย่างที่ 1

อย่างไรก็ตาม เนื่องจากกลยุทธ์ *ความจุของสถานที่เก็บสูงสุด* พยายามสร้างรหัสงานเนื่องจากไม่ได้อยู่ในตัวอย่างที่ 1 อาจล้มเหลว ในจุดนั้น ระบบจะพยายามกู้คืน

ทั้งนี้ขึ้นอยู่กับการตั้งค่าตัวเลือก **อนุญาตการแบ่ง** บนคำสั่งสถานที่สำหรับการเบิกสินค้าที่มีการเติมสินค้า มีสองอย่างดังนี้

- ถ้ามีการตั้งค่าตัวเลือก **อนุญาตให้มีการแบ่ง** เป็น *ใช่* งานการเติมสินค้าต่อไปนี้จะถูกสร้างขึ้น:

    - **งานการเพิ่มเติมสินค้า 1:** เบิกสินค้า 4 กล่องจากสถานที่เก็บสินค้าจำนวนมากและใส่ไว้ในสถานที่เบิกสินค้า-001
    - **งานการเพิ่มเติมสินค้า 2:** เบิกสินค้า 4 กล่องจากสถานที่เก็บสินค้าจำนวนมากและใส่ไว้ในสถานที่เบิกสินค้า-002

- ถ้ามีการตั้งค่าตัวเลือก **อนุญาตให้มีการแบ่ง** เป็น *ไม่* งานการเติมสินค้าต่อไปนี้จะถูกสร้างขึ้น:

    - **งานการเพิ่มเติมสินค้า 1:** เบิกสินค้า 4 กล่องจากสถานที่เก็บสินค้าจำนวนมากและใส่ไว้ในสถานที่เบิกสินค้า-001
    - **งานการเพิ่มเติมสินค้า 2:** เบิกสินค้า 2 กล่องจากสถานที่เก็บสินค้าจำนวนมากและใส่ไว้ในสถานที่เบิกสินค้า-002

ผลลัพธ์แตกต่างกันเนื่องจากข้อมูลที่สามารถใช้ได้เมื่อคุณสร้างงาน เมื่อมีการตั้งค่า **อนุญาตให้มีการแบ่ง** เป็น *ใช่* บนคำสั่งสถานที่สำหรับการเบิกสินค้าที่มีการเติมสินค้า คุณจะพบสินค้า 160 รายการ ดังนั้น คุณจึงสามารถสร้างงานสำหรับปริมาณดังกล่าวได้ อย่างไรก็ตาม เมื่อมีการตั้งค่าตัวเลือก **อนุญาตให้มีการแบ่ง** เป็น *ไม่* คุณไม่ทราบเกี่ยวกับการมีอยู่ของ 160 ชิ้น เนื่องจากปริมาณพิเศษที่คุณตัดสินใจที่จะเติมสินค้าคือ 3 กล่อง คุณปล่อยปริมาณพิเศษดังกล่าวและลองปริมาณเดิมอีกครั้ง

[![ตัวอย่าง 2](media/ReplenTemp_example_2.png "ตัวอย่างที่ 2")](media/ReplenTemp_example_2_large.png)

ดังนั้น เพื่อให้ได้ปริมาณสูงสุดสำหรับสถานที่ที่เติมสินค้า คุณควรตั้งค่าตัวเลือก **อนุญาตให้แบ่งได้** เป็น *ใช่* บนคำสั่งสถานที่สำหรับการเบิกสินค้าที่เพิ่มเติม


[!INCLUDE[footer-include](../../includes/footer-banner.md)]