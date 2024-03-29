---
title: ทำงานกับคำสั่งสถานที่ทำงาน
description: บทความนี้อธิบายวิธีการทำงานกับคำสั่งสถานที่ทำงาน คำสั่งสถานที่มีกฎที่กำหนดโดยผู้ใช้ซึ่งช่วยในการระบุการเบิกสินค้า และกำหนดสถานที่เก็บสำหรับการย้ายสินค้าคงคลัง
author: Mirzaab
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSLocDirHint, WHSLocDirTableUOM, WHSLocDirFailure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4ef8ec0732cd3bd50bca8d334c43d0354e9e3316
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689678"
---
# <a name="work-with-location-directives"></a>ทำงานกับคำสั่งสถานที่ทำงาน

[!include [banner](../includes/banner.md)]

คำสั่งสถานที่มีกฎซึ่งช่วยให้ระบุการเบิกสินค้าและกำหนดสถานที่เก็บสำหรับการย้ายสินค้าคงคลัง ตัวอย่างเช่น ในธุรกรรมใบสั่งขาย คำสั่งสถานกำหนดจุดที่จะเบิกสินค้า และจุดที่จะวางสินค้าที่เบิก คำสั่งที่ตั้งประกอบด้วยหัวข้อและบรรทัดที่เกี่ยวข้อง ซึ่งถูกสร้างสำหรับ *ชนิดของใบสั่งงาน* ที่ระบุ

> [!NOTE]
> บทความนี้จะใช้กับลักษณะการทำงานในโมดูล **การบริหารคลังสินค้า** หัวข้อนี้จะไม่ใช้กับคุณลักษณะในโมดูล [การบริหารคลังสินค้า](../inventory/inventory-home-page.md)

คุณสามารถใช้คำสั่งสถานที่เพื่อทำงานต่อไปนี้:

- ย้ายเก็บสินค้าขาเข้า
- เบิกและแสดงสินค้าสำหรับธุรกรรมขาออก
- เบิกและวางวัตถุดิบสำหรับการผลิต
- เพิ่มเติมสถานที่

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่คุณสามารถสร้างคำสั่งสถานที่ คุณต้องปฏิบัติตามขั้นตอนเหล่านี้เพื่อให้แน่ใจว่ามีข้อกำหนดเบื้องต้นอยู่

1. ตรวจสอบให้แน่ใจว่ามีการเปิดใช้งานคีย์ลิขสิทธิ์ที่จำเป็นอยู่ ให้ไปที่ **การจัดการระบบ \> ตั้งค่า \> การตั้งค่าคอนฟิกลิขสิทธิ์** ขยาย คีย์ลิขสิทธิ์ **ทางการค้า** แล้วเลือก คีย์การตั้งค่าคอนฟิก **การจัดการคลังสินค้าและการขนส่ง** โปรดทราบว่าจำเป็นต้องมีการเข้าถึงของผู้ดูแลระบบสำหรับขั้นตอนนี้
1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> คลังสินค้า**
1. การสร้างคลังสินค้า
1. บนแท็บด่วน **คลังสินค้า** ให้ตั้งค่าตัวเลือก **ใช้กระบวนการจัดการคลังสินค้า** เป็น *ใช่*
1. สร้างสถานที่ ชนิดสถานที่ โพรไฟล์สถานที่ และรูปแบบสถานที่ สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ตั้งค่าคอนฟิกสถานที่ในคลังสินค้าที่เปิดใช้งาน WMS](./tasks/configure-locations-wms-enabled-warehouse.md)
1. สร้างไซต์ เขต และกลุ่มเขต สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [การตั้งค่าคลังสินค้า](../../commerce/channels-setup-warehouse.md) และ [ตั้งค่าคอนฟิกสถานที่ในคลังสินค้าที่เปิดใช้งาน WMS](./tasks/configure-locations-wms-enabled-warehouse.md)

## <a name="turn-the-location-directive-scopes-feature-on-or-off"></a><a name="scopes-feature"></a>เปิดหรือปิดคุณลักษณะขอบเขตคำสั่งสถานที่

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until 10.0.31 GA -->

คุณลักษณะ *ขอบเขตคำสั่งสถานที่* ช่วยให้คุณมีอิสระมากขึ้นเมื่อคุณออกแบบคำสั่งสถานที่และช่วยลดการตั้งค่าคอนฟิกที่ซ้ำซ้อน โดยจะเพิ่มตัวเลือก **ขอบเขต** ซึ่งแทนที่ตัวเลือก **หลาย SKU** ก่อนหน้านี้ ในขณะที่สามารถตั้งค่าตัวเลือก **หลาย SKU** เป็น *ใช่* หรือ *ไม่* ได้เท่านั้น ตัวเลือก **ขอบเขต** จะให้การตั้งค่าสองค่าดังกล่าว (โดยผ่านค่า *สินค้าเดียว* และ *สินค้าหลายรายการ*) แต่ยังมีอีกสองค่าเพิ่มเติม (โดยผ่านค่า *สินค้าหรือใบสั่งรายการเดียว* และค่า *ทั้งหมด*) หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าเหล่านี้ ดูที่ [แท็บด่วนคำสั่งสถานที่](#location-directives-tab)

เมื่อเปิดใช้งาน ตัวเลือก **ขอบเขต** จะแทนที่ตัวเลือก **หลาย SKU** และเข้ากันได้กับการตั้งค่าคอนฟิกที่มีอยู่ 100 เปอร์เซ็นต์

การใช้คุณลักษณะนี้ คุณต้องเปิดคุณลักษณะนี้ในระบบของคุณก่อน ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะและเปิดหรือปิดใช้งาน ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:

- **โมดูล:** *การจัดการคลังสินค้า*
- **ชื่อคุณลักษณะ:** *ขอบเขตคำสั่งสถานที่*

## <a name="work-order-types-for-location-directives"></a>ชนิดของใบสั่งงานสำหรับคำสั่งสถานที่

มีฟิลด์จำนวนมากที่สามารถตั้งค่าสำหรับคำสั่งสถานที่ ที่ใช้ทั่วไปสำหรับชนิดของใบสั่งงานทั้งหมด อย่างไรก็ตาม ฟิลด์อื่นๆ มีเฉพาะสำหรับชนิดของใบสั่งงานเฉพาะ

![ชนิดของใบสั่งงานคำสั่งสถานที่](media/Location_Directives_Work_Order_Types.png "ชนิดของใบสั่งงานคำสั่งสถานที่")

> [!NOTE]
> ชนิดของใบสั่งงานสองชนิด *งานที่ถูกยกเลิก* และ *การตรวจนับตามรอบ* จะใช้โดยระบบเท่านั้น ไม่สามารถสร้างคำสั่งสถานที่สำหรับชนิดใบสั่งงานเหล่านี้ได้

ตารางในส่วนย่อยต่อไปนี้จะแสดงรายการชนิดของใบสั่งทั่วไปและผู้ปฏิบัติงาน–เฉพาะฟิลด์ที่พร้อมใช้งานเมื่อคุณตั้งค่าคำสั่งสถานที่

### <a name="fields-that-are-common-to-all-work-order-types"></a>ฟิลด์ที่ใช้ทั่วไปสำหรับชนิดใบสั่งงานทั้งหมด

ตารางต่อไปนี้แสดงรายการฟิลด์ที่ใช้ทั่วไปสำหรับชนิดของใบสั่งงานทั้งหมด

| แท็บด่วน | ฟิลด์ |
|---|---|
| คำสั่งสถานที่ | ชนิดของงาน |
| คำสั่งสถานที่ | ไซต์ |
| คำสั่งสถานที่ | คลังสินค้า |
| คำสั่งสถานที่ | รหัสคำสั่ง |
| คำสั่งสถานที่ | ขอบเขต *หรือ* หลาย SKU |
| รายการ | หมายเลขลำดับ |
| รายการ | ปริมาณเริ่มต้น |
| รายการ | ปริมาณสิ้นสุด |
| รายการ | หน่วย |
| รายการ | ค้นหาปริมาณ |
| รายการ | จำกัดตามหน่วย |
| รายการ | ปัดเป็นหน่วย |
| รายการ | ระบุตำแหน่งปริมาณการบรรจุ |
| รายการ | อนุญาตให้แบ่งได้ |
| การดำเนินการคำสั่งสถานที่ | หมายเลขลำดับ |
| การดำเนินการคำสั่งสถานที่ | ชื่อ |
| การดำเนินการคำสั่งสถานที่ | การใช้สถานที่คงที่ |
| การดำเนินการคำสั่งสถานที่ | อนุญาตสินค้าคงคลังค่าลบ |
| การดำเนินการคำสั่งสถานที่ | เปิดใช้งานชุดงาน |
| การดำเนินการคำสั่งสถานที่ | กลยุทธ์ |

### <a name="fields-that-are-specific-to-work-order-types"></a><a name="fields-specific-types"></a>ฟิลด์ที่เฉพาะสำหรับชนิดใบสั่งงาน

ตารางต่อไปนี้แสดงรายการฟิลด์ที่เฉพาะสำหรับชนิดของใบสั่งงานที่ระบุ

| แท็บด่วน | ฟิลด์ | ชนิดใบสั่งงาน |
|---|---|---|
| คำสั่งสถานที่ | ค้นหาตาม | ใบสั่งซื้อ |
| คำสั่งสถานที่ | รหัสการโอนการครอบครองที่เกี่ยวข้อง | ใบสั่งซื้อ |
| คำสั่งสถานที่ | รหัสการโอนการครอบครอง | ใบสั่งซื้อ |
| คำสั่งสถานที่ | รหัสการโอนการครอบครองที่เกี่ยวข้อง | การสำรองสินค้าที่สำเร็จแล้ว |
| คำสั่งสถานที่ | รหัสการโอนการครอบครอง | การสำรองสินค้าที่สำเร็จแล้ว |
| คำสั่งสถานที่ | รหัสการโอนการครอบครองที่เกี่ยวข้อง | ใบสั่งส่งคืนสินค้า |
| คำสั่งสถานที่ | รหัสการโอนการครอบครอง | ใบสั่งส่งคืนสินค้า |
| คำสั่งสถานที่ | รหัสการโอนการครอบครองที่เกี่ยวข้อง | การสำรองสินค้าคัมบัง |
| คำสั่งสถานที่ | รหัสการโอนการครอบครองที่เกี่ยวข้อง | การเบิกสินค้าคัมบัง |
| รายการ | เทมเพลตการเติมสินค้าทันที | ใบสั่งขาย |
| รายการ | เทมเพลตการเติมสินค้าทันที | การเบิกวัตถุดิบ |
| รายการ | เทมเพลตการเติมสินค้าทันที | โอนย้ายการตัดสินค้า |
| รายการ | เทมเพลตการเติมสินค้าทันที | การเบิกสินค้าคัมบัง |

## <a name="open-the-location-directives-page"></a>เปิดหน้าคำสั่งสถานที่

การเปิดหน้า **คำสั่งสถานที่** ให้ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คำสั่งสถานที่**

จากที่นั่น คุณสามารถดู สร้าง และแก้ไขคำสั่งสถานที่ของคุณได้ โดยใช้คำสั่งบนบานหน้าต่างการดำเนินการ ดูส่วนที่เหลือของบทความนี้สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้ฟิลด์ทั้งหมดที่พร้อมใช้งานบนหน้า

## <a name="action-pane"></a>บานหน้าต่างการดำเนินการ

บานหน้าต่างการดำเนินการ บนหน้า **คำสั่งสถานที่** มีปุ่มที่คุณสามารถใช้ในการสร้าง แก้ไข และลบคำสั่ง (**แก้ไข** **สร้าง** และ **ลบ**) นอกจากนี้ยังมีปุ่มต่อไปนี้ซึ่งช่วยให้คุณสามารถปรับปรุงลำดับที่มีการประมวลผลคำสั่งสถานที่ และตั้งค่าคอนฟิกการสอบถามที่กำหนดเงื่อนไขสำหรับการใช้คำสั่งสถานที่:

- **เลื่อนขึ้น** – เลื่อนคำสั่งสถานที่ที่เลือกขึ้นในลำดับ ตัวอย่างเช่น คุณสามารถย้ายจากหมายเลขลำดับ 4 ไปยังหมายเลขลำดับ 3
- **เลื่อนลง** – เลื่อนคำสั่งสถานที่ที่เลือกลงในลำดับ ตัวอย่างเช่น คุณสามารถย้ายจากหมายเลขลำดับ 4 ไปยังหมายเลขลำดับ 5
- **คัดลอก** – เปิดกล่องโต้ตอบ ซึ่งคุณสามารถสร้างสําเนาที่แน่นอนของคำสั่งสถานที่ปัจจุบันได้
- **แก้ไขการสอบถาม** – เปิดกล่องโต้ตอบที่คุณสามารถกำหนดเงื่อนไขที่ควรมีการประมวลผลคำสั่งของสถานที่ที่เลือกภายใต้ ตัวอย่างเช่น คุณอาจต้องการให้นำไปใช้กับคลังสินค้าที่ระบุเท่านั้น
- **การทดสอบการยอมรับ** – เปิดหน้าซึ่งคุณสามารถตั้งค่าการทดสอบอัตโนมัติ เพื่อระบุว่าคำสั่งสถานที่ของคุณจะอยู่ภายใต้เงื่อนไขการเริ่มต้นที่แตกต่างกันอย่างไร ด้วยวิธีนี้ คุณจะสามารถตรวจสอบความถูกต้องของคำสั่งที่คุณป้อนไว้ได้อย่างรวดเร็วเมื่อสร้างและเก็บรักษา หากต้องการทราบข้อมูลเพิ่มเติม โปรดดูที่ [ทดสอบคำสั่งสถานที่กับการทดสอบการยอมรับ](location-directive-acceptance-tests.md)

## <a name="location-directives-header"></a>หัวข้อคำสั่งสถานที่

ส่วนหัวของคำสั่งสถานที่มีฟิลด์ต่อไปนี้สำหรับหมายเลขลำดับและชื่อที่อธิบายของคำสั่งสถานที่:

- **หมายเลขลำดับ** – ฟิลด์นี้บ่งชี้ถึงลำดับที่ระบบพยายามใช้คำสั่งของสถานที่แต่ละรายการ สำหรับชนิดของใบสั่งงานที่เลือก หมายเลขต่ำจะถูกใช้เป็นอันดับแรก คุณสามารถเปลี่ยนลำดับได้โดยการใช้ปุ่ม **เลื่อนขึ้น** และ **เลื่อนลง** ในบานหน้าต่างการดำเนินการ
- **ชื่อ** - ให้ป้อนชื่อที่เป็นคำอธิบายสำหรับคำสั่งสถานที่ ชื่อนี้ควรช่วยระบุวัตถุประสงค์ทั่วไปของคำสั่ง ตัวอย่างเช่น ป้อน *การเบิกสินค้าตามใบสั่งขายในคลังสินค้า 24*

## <a name="location-directives-fasttab"></a><a name="location-directives-tab"></a>ปุ่มด่วนคำสั่งสถานที่

ฟิลด์บนแท็บด่วน **คำสั่งสถานที่ต** ใช้สำหรับชนิดของใบสั่งงานที่เลือกไว้ในฟิลด์ **ชนิดของใบสั่งงาน** ในบานหน้าต่างรายการ

- **ชนิดงาน** – เลือกชนิดของงานที่ต้องดำเนินการ ค่าที่ใช้ได้จะขึ้นอยู่กับชนิดของธุรกรรมสินค้าคงคลังที่คุณเลือกในฟิลด์ **ชนิดใบสั่งงาน** เลือกค่าใดค่าหนึ่งต่อไปนี้

    - **ส่งสินค้า** – คำสั่งสถานที่จะพยายามหาสถานที่ที่เหมาะสมที่สุดในการส่งสินค้าหรือระบุตำแหน่งสินค้าคงคลังที่เข้ามาในระบบจากการรับสินค้า การผลิต หรือการปรับปรุงสินค้าคงคลัง นอกจากนี้ ยังสามารถใช้เพื่อกำหนดตำแหน่งการวางไปยังที่ที่ตั้งระยะ หรือสถานที่จัดส่งในพื้นที่ประตูสุดท้าย
    - **เบิกสินค้า** – คำสั่งสถานที่จะพยายามหาสถานที่ที่เหมาะสมที่สุดสำหรับการสำรองสินค้าคงคลังจริงจาก (นั่นคือ สร้างงาน) สามารถดำเนินการเบิกสินค้าให้เสร็จสิ้นได้ (นั่นคือรายการงานการเบิกสินค้าสามารถถูกปิดได้) แม้ว่างานจะยังไม่เสร็จสมบูรณ์ ผู้ใช้สามารถทำการเบิกสินค้าจริงได้ ในระบบ การดำเนินการดังกล่าวเป็นขั้นตอนการเบิกสินค้า จากนั้น ผู้ใช้สามารถยกเลิกได้จากอุปกรณ์เคลื่อนที่ และทำงานให้เสร็จสมบูรณ์ในภายหลัง อย่างไรก็ตาม ส่วนหัวของงานถูกปิดก่อน เมื่อเสร็จสิ้นการเก็บสินค้าขั้นสุดท้ายเสร็จสมบูรณ์

    > [!IMPORTANT]
    > ค่าอื่นๆ ในฟิลด์ **ชนิดงาน** ไม่เกี่ยวข้องกับคำสั่งสถานที่ ฟิลด์นี้จะปรากฏเฉพาะเนื่องจากไม่มีการกรองข้อมูลฟิลด์เพื่อให้ตรงกับชนิดของใบสั่งงานที่เลือก

- **ไซต์** – ฟิลด์นี้เป็นฟิลด์บังคับ เนื่องจากคำสั่งสถานที่จำเป็นต้องกำหนดไซต์และคลังสินค้าที่ถูกต้อง
- **คลังสินค้า** – ฟิลด์นี้เป็นฟิลด์บังคับ เนื่องจากคำสั่งสถานที่จำเป็นต้องกำหนดไซต์และคลังสินค้าที่ถูกต้อง
- **รหัสคำสั่ง** – เลือกรหัสคำสั่งเพื่อเชื่อมโยงกับเทมเพลตงานหรือเทมเพลตการเติมสินค้า บนหน้า **รหัสคำสั่ง** คุณสามารถสร้างรหัสใหม่ที่สามารถใช้ในการเชื่อมต่อเทมเพลตงานหรือเทมเพลตการเติมสินค้ากับคำสั่งสถานที่ รหัสคำสั่งยังสามารถใช้หน้านั้นเพื่อสร้างการเชื่อมโยงระหว่างรายการเทมเพลตงานใดๆ และคำสั่งสถานที่ (เช่น พื้นที่ประตูหรือที่ตั้งระยะ)

    > [!TIP]
    > ถ้ามีการกำหนดรหัสคำสั่ง ระบบจะไม่ค้นหาคำสั่งสถานที่ตามหมายเลขลำดับ เมื่องานต้องถูกสร้างขึ้น แต่จะค้นหาตามรหัสคำสั่งแทน สำหรับวิธีนี้ คุณสามารถระบุได้มากขึ้นเกี่ยวกับคำสั่งสถานที่ที่มีการใช้สำหรับขั้นตอนที่ระบุในแม่แบบงาน เช่น ขั้นตอนสำหรับการจัดเตรียมวัสดุ

- **ขอบเขต** – ใช้ตัวเลือกนี้เพื่อระบุสถานการณ์ที่จะมีการใช้คำสั่งสถานที่ ตัวเลือกนี้จะแทนที่ตัวเลือก **หลาย SKU** และจะพร้อมใช้งานเฉพาะเมื่อคุณลักษณะ *ขอบเขตคำสั่งสถานที่* เปิดอยู่ในระบบของคุณ (สำหรับข้อมูลเพิ่มเติม ดูที่ [เปิดหรือปิดคุณลักษณะของขอบเขตคำสั่งสถานที่](#scopes-feature))

    | การตั้งค่าขอบเขต | ใบสั่งเดียวที่มีสินค้าเพียงรายการเดียว | ใบสั่งหลายรายการที่มีสินค้าเดียวกัน | ใบสั่งเดียวที่มีสินค้าหลายรายการ | ใบสั่งหลายรายการที่มีสินค้าหลายรายการ |
    |---|---|---|---|---|
    | สินค้ารายการเดียว | ใช่ | ใช่ | หมายเลข | หมายเลข |
    | สินค้าหลายรายการ | หมายเลข | หมายเลข | ใช่ | ใช่ |
    | สินค้าหรือใบสั่งรายการเดียว | ใช่ | ใช่ | ใช่ | หมายเลข |
    | ทั้งหมด | ใช่ | ใช่ | ใช่ | ใช่ |

    ตารางต่อไปนี้จะอธิบายว่าขอบเขตพร้อมใช้งานเมื่อใด และอนุญาตให้มีการใช้ฟังก์ชัน **Edit query** หรือไม่

    | ขอบเขต | ชนิดงานที่สนับสนุน | ชนิดใบสั่งงานที่สนับสนุน | อนุญาตให้แก้ไขการสอบถามได้ |
    |---|---|---|---|
    | สินค้ารายการเดียว | ทั้งหมด | ทั้งหมด | ใช่ |
    | สินค้าหลายรายการ | ทั้งหมด | ทั้งหมด | หมายเลข |
    | สินค้าหรือใบสั่งรายการเดียว | การสำรองสินค้า | การสำรองผลิตภัณฑ์ร่วมและการสำรองสินค้าพลอยได้ การสำรองสินค้าสำเร็จรูป การสำรองสินค้าคัมบัง ใบสั่งซื้อ ใบสั่งตรวจสอบคุณภาพ การเติมสินค้า ใบสั่งส่งคืนสินค้า ใบสั่งขาย การออกใช้การโอนย้า และการรับสินค้าจากการโอนย้าย | ใช่ |
    | ทั้งหมด | การสำรองสินค้า | ทั้งหมด | หมายเลข |

    > [!NOTE]
    > - หากต้องการสำรองสินค้าไว้ทั้งสินค้าหลายรายการและสินค้าเดียว คุณต้องตรวจสอบให้แน่ใจว่ามีคำสั่งสถานที่ซึ่งครอบคลุมทั้งสองสถานการณ์ ตัวอย่างเช่น คุณอาจตั้งค่าคำสั่งสถานที่ *สินค้าหรือใบสั่งรายการเดียว* เพื่อครอบคลุมสถานการณ์ที่ต้องมีการปรับแต่ง (เช่น โดยผ่านการแก้ไขในการสอบถาม) แล้วจากนั้นก็หนึ่งคำสั่งสถานที่ขึ้นไปใน *ทั้งหมด* เพื่อครอบคลุมสถานการณ์คงเหลือ
    > - ถึงแม้ว่าคุณจะสามารถใช้ *สินค้ารายการเดียว* และ *สินค้าหลายรายการ* กับการสำรองสินค้า แต่วิธีการนี้มักจะใช้ในการกําหนดโครงแบบที่ซ้ำซ้อน พิจารณาการใช้ขอบเขต *สินค้าหรือใบสั่งรายการเดียว* หรือ *ทั้งหมด* แทน เนื่องจากวิธีการนี้จะก่อให้เกิดการตั้งค่าเริ่มต้นใหม่

- **หลาย SKU** – ใช้ตัวเลือกนี้เพื่อระบุสถานการณ์ที่จะมีการใช้คำสั่งสถานที่ การตั้งค่านี้จะถูกแทนที่ด้วยการตั้งค่า **ขอบเขต** ถ้าคุณลักษณะ *ขอบเขตคำสั่งสถานที่* เปิดอยู่ในระบบของคุณ (สำหรับข้อมูลเพิ่มเติม ดูที่ [เปิดหรือปิดคุณลักษณะของขอบเขตคำสั่งสถานที่](#scopes-feature)) ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อเปิดใช้งานหหน่วยการเก็บสินค้าคงคลัง (SKU) หลายหน่วยที่จะใช้ในสถานที่ ตัวอย่างเช่น ต้องเปิดใช้งานหลาย SKU สำหรับสถานที่พื้นที่ประตู ถ้าคุณเปิดใช้งานหลาย SKU สถานที่ของคุณจะได้รับการระบุในงาน ตามที่คาดไว้ อย่างไรก็ตาม สถานที่เก็บจะสามารถจัดการกับการจัดส่งสินค้าหลายรายการ (ถ้างานรวมถึง SKU ที่แตกต่างกันที่ต้องมีการเบิกสินค้าและการวาง) การดำเนินการนี้จะไม่สามารถจัดการการวาง SKU แบบเดี่ยวได้ ถ้าคุณกำหนดตัวเลือกนี้เป็น *ไม่* สถานที่ส่งของคุณจะได้รับการระบุเฉพาะเมื่อการส่งของคุณมี SKU เพียงหนึ่งชนิดเท่านั้น

    > [!IMPORTANT]
    > เมื่อต้องการให้สามารถดำเนินการทั้งการส่งแบบหลายรายการ และการส่งแบบ SKU เดียว คุณต้องระบุสองบรรทัดที่มีโครงสร้างและการตั้งค่าเดียวกัน แต่คุณต้องตั้งค่าตัวเลือก **SKU หลายรายการ** เป็น *ใช่* สำหรับหนึ่งบรรทัด และ *ไม่* สำหรับอีกบรรทัดหนึ่ง ดังนั้น สำหรับการดำเนินการส่งสินค้า คุณต้องมีสองคำสั่งสถานที่ ถึงแม้ว่าคุณจะไม่ต้องแยกระหว่าง SKUsแบบรายการเดียว หรือหลายรายการในรหัสงาน บ่อยครั้ง ถ้าคุณไม่ได้ตั้งค่าคำสั่งสถานที่เหล่านี้ ที่ตั้งกระบวนการทางธุรกิจที่ไม่คาดคิดจะมาจากคำสั่งสถานที่ที่ใช้ คุณต้องใช้การตั้งค่าที่คล้ายกันสำหรับคำสั่งสถานที่ที่มี **ชนิดงาน** ของ *การเบิกสินค้า* ถ้าคุณต้องการประมวลผลใบสั่งที่มีหลาย SKU

    ใช้ตัวเลือก **SKU หลายรายการ** สำหรับรายการงานที่จัดการหมายเลขสินค้ามากกว่าหนึ่งหมายเลข (หมายเลขสินค้าจะว่างเปล่าในรายละเอียดงาน และจะแสดงเป็น **หลายรายการ** บนหน้าการประมวลผลในแอปการจัดการคลังสินค้าบนมือถือ)

    ในสถานการณ์ตัวอย่างโดยทั่วไป เทมเพลตงานจะถูกตั้งค่าเพื่อให้มีการเบิกสินค้า/การจับคู่ มากกว่าหนึ่งรายการ ในกรณีนี้ คุณอาจต้องการค้นหาสถานที่การแบ่งระยะที่เฉพาะเจาะจงที่จะใช้สำหรับบรรทัดที่มี **ชนิดงาน** ของ *การส่ง*

    > [!NOTE]
    > ถ้าตัวเลือก **SKU หลายรายการ** ถูกตั้งค่าเป็น *ใช่* คุณจะไม่สามารถเลือก **แก้ไขการสอบถาม** บนบานหน้าต่างการดำเนินการได้ เนื่องจากการสอบถามไม่สามารถประเมินในระดับสินค้าได้เมื่อมีสินค้าหลายรายการ เมื่อต้องการตรวจสอบให้แน่ใจว่ามีการเลือกคำสั่งสถานที่ที่ต้องการแล้ว ให้ใช้ฟิลด์ **รหัสคำสั่ง** เพื่อแนะนำการเลือกคำสั่งของสถานที่ที่เกี่ยวข้องกับบรรทัดการส่งที่มีการกำหนดรหัสคำสั่งนี้ไว้ในเทมเพลตงาน

    เว้นแต่คุณจะทำงานกับการดำเนินงานที่มีสินค้าหนึ่งรายการหรือสินค้าผสมอย่างใดอย่างหนึ่ง จำเป็นที่คุณต้องกำหนดคำสั่งสถานที่สองคำสั่งสำหรับชนิดงาน: *การส่ง* หนึ่งคำสั่งสำหรับการตั้งค่าตัวเลือก **SKU หลายรายการ** เป็น *ใช่* และอีกหนึ่งสำหรับตั้งค่าเป็น *ไม่*

- **รหัสการโอนการครอบครองที่ถูกต้อง** –ระบุว่ารหัสการโอนการครอบครองของคำสั่งสถานที่ต้องตรงกับรหัสการโอนการครอบครองที่ใช้เมื่อได้รับสินค้า หรือคำสั่งสถานที่สามารถเลือกได้ตามรหัสการโอนการครอบครองใดๆ ถ้าคุณเลือก *การจับคู่ที่ตรงกัน* และฟิลด์ **รหัสการโอนการครอบครอง** ว่างเปล่า จะมีการพิจารณาเฉพาะรหัสการโอนการครอบครองที่ว่างเปล่าสำหรับคำสั่งสถานที่นี้

    > [!NOTE]
    > ฟิลด์นี้จะพร้อมใช้งานสำหรับชนิดของใบสั่งงานที่เลือกเท่านั้นที่จะได้รับการเติมสินค้า สำหรับรายการทั้งหมด ให้ดู [ฟิลด์ที่ระบุให้กับชนิดของใบสั่งงาน](#fields-specific-types) ส่วนก่อนหน้านี้ในบทความนี้

- **ค้นหาโดย** – ระบุว่าปริมาณ putaway ควรจะเป็นปริมาณทั้งหมดบนป้ายทะเบียน หรือว่าควรจะเป็นสินค้าตามสินค้าหรือไม่ ใช้ฟิลด์นี้เพื่อช่วยให้มั่นใจว่าเนื้อหาทั้งหมดบนป้ายทะเบียนถูกวางลงในสถานที่หนึ่ง และระบบไม่แนะนำให้คุณแบ่งเนื้อหาออกเป็นหลายสถานที่สำหรับ **ASN** (ป้ายทะเบียนที่ได้รับ) การรับสินค้า **ป้ายทะเบียนแบบผสม** และกระบวนการรับสินค้า **คลัสเตอร์** (กระบวนการรับ **คลัสเตอร์** ต้องมีการเปิดใช้งาน [การสำรองสินค้าของคลัสเตอร์](putaway-clusters.md)) ลักษณะการทำงานของการสอบถามคำสั่งสถานที่ บรรทัด และการดำเนินการคำสั่งสถานที่จะแตกต่างกันไป ขึ้นอยู่กับค่าที่คุณเลือก แท็บด่วน **บรรทัด** จะใช้เฉพาะเมื่อมีการตั้งค่า **ค้นหาตาม** เป็น *สินค้า*

    > [!NOTE]
    > ฟิลด์นี้จะพร้อมใช้งานสำหรับชนิดของใบสั่งงานที่เลือกเท่านั้นที่จะได้รับการเติมสินค้า สำหรับรายการทั้งหมด ให้ดูส่วน [ฟิลด์ที่ระบุให้กับชนิดของใบสั่งงาน](#fields-specific-types)

- **รหัสการโอนการครอบครอง** – ฟิลด์นี้จะใช้สำหรับคำสั่งสถานที่ที่มีชนิดใบสั่งงานของ *ใบสั่งซื้อ* *การสำรองสินค้าสำเร็จรูป* หรือ *ใบสั่งส่งคืนสินค้า* และชนิดของงานที่ *วาง* ใช้เพื่อแนะนำขั้นตอนในการใช้คำสั่งสถานที่เฉพาะ ทั้งนี้ขึ้นอยู่กับรหัสการโอนการครอบครองซึ่งผู้ปฏิบัติงานที่เลือกไว้ในแอปการจัดการคลังสินค้าบนมือถือ ตัวอย่างเช่น คุณสามารถส่งคืนสินค้าไปยังสถานที่ตรวจสอบก่อนที่จะส่งคืนไปยังสินค้าคงคลังได้ รหัสการโอนการครอบครองสามารถเชื่อมโยงกับสถานะของสินค้าคงคลังได้ ด้วยวิธีนี้คุณสามารถใช้เพื่อเปลี่ยนสถานะสินค้าคงคลังเป็นส่วนหนึ่งของกระบวนการรับได้ ตัวอย่างเช่น คุณมีรหัสการโอนการครอบครอง *QA* ที่ตั้งค่าสถานะสินค้าคงคลังเป็น *QA* จากนั้นคุณสามารถมีคำสั่งสถานที่แยกต่างหากเพื่อย้ายสินค้าคงคลังไปยังสถานที่ตรวจสอบสินค้า

    > [!NOTE]
    > ฟิลด์นี้จะพร้อมใช้งานสำหรับชนิดของใบสั่งงานที่เลือกเท่านั้นที่จะได้รับการเติมสินค้า สำหรับรายการทั้งหมด ให้ดูส่วน [ฟิลด์ที่ระบุให้กับชนิดของใบสั่งงาน](#fields-specific-types)

## <a name="lines-fasttab"></a>แท็บด่วนรายการ

ใช้แท็บด่วน **รายการ** เพื่อกำหนดเงื่อนไขสำหรับการใช้การดำเนินการที่เกี่ยวข้องที่ระบุไว้ในแท็บด่วน **การดำเนินการคำสั่งสถานที่** สำหรับแต่ละรายการ คุณสามารถระบุปริมาณต่ำสุดและปริมาณสูงสุดที่ควรใช้การดำเนินการ นอกจากนี้ คุณยังสามารถระบุได้ว่าควรใช้การดำเนินการสำหรับหน่วยสินค้าคงคลังเฉพาะหรือไม่

- **หมายเลขลำดับ** - ป้อนลำดับที่ควรจะมีการดำเนินการคำสั่งสถานที่แต่ละรายการสำหรับชนิดงานที่เลือก คุณสามารถเปลี่ยนลำดับได้ตามต้องการโดยการใช้ปุ่ม **เลื่อนขึ้น** และ **เลื่อนลง** บนแถบเครื่องมือ
- **ปริมาณเริ่มต้น** – ระบุจุดเริ่มต้นของช่วงของปริมาณที่จะใช้กับรายการ ระบุปริมาณในหน่วยวัดที่เลือกไว้ในฟิลด์ **หน่วย**
- **ปริมาณสิ้นสุด** – ระบุจุดสิ้นสุดของช่วงของปริมาณที่จะใช้กับรายการ ระบุปริมาณในหน่วยวัดที่เลือกไว้ในฟิลด์ **หน่วย**
- **หน่วย** – เลือกหน่วยวัดของรายการ คุณสามารถระบุปริมาณต่ำสุดและปริมาณสูงสุดที่คำสั่งควรใช้กับ และคุณสามารถระบุว่าควรมีคำสั่งสำหรับเฉพาะหน่วยสินค้าคงคลังหรือไม่ ฟิลด์ **หน่วย** จะใช้ *เฉพาะ* สำหรับการประเมินปริมาณเท่านั้น เมื่อต้องการตรวจสอบว่ารายการคำสั่งสถานที่เหมาะสมหรือไม่ ระบบจะใช้ปริมาณในหน่วยที่ระบุไว้ในรายการนั้น ทุกครั้งที่เข้าถึงรายการคำสั่งสถานที่ ระบบจะพยายามแปลงหน่วยความต้องการไปยังหน่วยที่ระบุในรายการ ถ้าไม่มีการสนทนาหน่วยวัด ระบบจะเลื่อนไปยังรายการถัดไป
- **ค้นหาปริมาณ** - ฟิลด์นี้จะใช้เฉพาะระหว่างความพยายามในการวางหรือค้นหาสินค้าในคลังสินค้า (ดังนั้น จะใช้ได้เฉพาะเมื่อมีการตั้งค่าฟิลด์ **ชนิดงาน** เป็น *เก็บสินค้า* เท่านั้น) เลือกค่าอย่างใดอย่างหนึ่งต่อไปนี้เพื่อระบุปริมาณที่ใช้ในการประเมินว่าปริมาณจะอยู่ภายในช่วง **ปริมาณเริ่มต้น** ถึง **ปริมาณสิ้นสุด** หรือไม่

    - **ปริมาณป้ายทะเบียน** – ใช้ปริมาณบนป้ายทะเบียนที่ได้รับ
    - **ปริมาณรวมไว้** – ใช้ปริมาณที่จะใช้ในระหว่างธุรกรรม ตัวอย่างเช่น คุณจะได้รับปริมาณของ 1,000 ในคลังสินค้าและแบ่งออกเป็น ป้ายทะเบียน 10 แผ่น ซึ่งแต่ละแผ่น มีปริมาณ 100 ในกรณีนี้ คุณสามารถใช้ปริมาณของ 1,000 สินค้า แทนที่จะเป็นปริมาณป้ายทะเบียนของ 100
    - **ปริมาณคงเหลือ** – ใช้ปริมาณที่ต้องยังคงได้รับในรายการใบสั่งซื้อที่มีการประมวลผล
    - **ปริมาณที่คาดไว้** – ใช้ปริมาณรวมของรายการใบสั่งซื้อ โดยไม่คำนึงถึงสิ่งที่ได้รับแล้ว

- **จำกัดตามหน่วย** – กล่องกาเครื่องหมายนี้ช่วยให้คุณสามารถกำหนดรายการคำสั่งสถานที่เฉพาะสำหรับหน่วยวัดหรือหน่วยวัดต่างๆ เลือกกล่องกาเครื่องหมาย เพื่อจำกัดหน่วยวัดที่จะถือว่าเป็นเกณฑ์การเลือกที่ถูกต้องสำหรับรายการคำสั่งสถานที่ ฟังก์ชันนี้จะทำงานเฉพาะสำหรับคำสั่งสถานที่ที่ฟิลด์ **ชนิดงาน** มีการตั้งค่าเป็น *เบิกสินค้า* เท่านั้น

    ตัวอย่างเช่น เมื่อคุณจองปริมาณ คุณต้องการจองแท่นวางสินค้าจากชุดของสถานที่เฉพาะเท่านั้น ในกรณีนี้ บรายการจะจำกัดลำดับให้กับแท่นวางสินค้าในลักษณะที่มีการเลือกปริมาณที่น้อยกว่าแท่นวางสินค้าสำหรับคำสั่งสถานที่

    โปรดทราบว่า ในกล่องกาเครื่องหมาย **จำกัดตามหน่วย** จะไม่ควบคุมหน่วยที่ใช้กับรายการงาน การจำกัดหน่วยใช้กับหน่วยที่มีอยู่ผ่านทางกลุ่มลำดับของหน่วยเท่านั้น ตัวอย่างเช่น สินค้าเชื่อมโยงกับกลุ่มลำดับของหน่วยที่มีทั้งหน่วย *แท่นวางสินค้า* และหน่วย *ชิ้น* มีการกำหนดหน่วยวัด ให้ 1 แท่นวางสินค้า = 100 ชิ้น และคำสั่งสถานที่ใช้ฟังก์ชัน **จำกัดตามหน่วย** เท่านั้นสำหรับแท่นวางสินค้า นอกจากนี้ เทมเพลตงานได้รับการกำหนดให้จำกัดการสร้างส่วนหัวของงานเป็น 50 ชิ้น ในกรณีนี้ จะมีการสร้างรายการงาน 50 ชิ้น หากต้องการระบุหน่วยวัดสำหรับการจำกัด ให้ทำตามขั้นตอนดังนี้

    1. บนแท็บด่วน **รายการ** ให้เลือก **จำกัดตามหน่วย** บนแถบเครื่องมือ (ปุ่มนี้จะสามารถใช้ได้เฉพาะหลังจากที่คุณเลือกกล่องกาเครื่องหมาย **จำกัดตามหน่วย** ในรายการ แล้วเลือก **บันทึก**)
    1. บนหน้า **จำกัดตามหน่วย** ในฟิลด์ **หน่วย** ให้เลือกหน่วยวัดที่คุณต้องการจำกัดโดยใช้สำหรับกระบวนการการเบิกสินค้าและการวาง

- **การปัดเศษขึ้นเป็นหน่วย** – ฟิลด์นี้จะทำงานร่วมกับกล่องกาเครื่องหมาย **จำกัดตามหน่วย** ตัวอย่างเช่น ถ้ามีการเลือกรายการคำสั่งสถานที่ **จำกัดตามหน่วย** และ **ปัดเป็นหน่วย** งานที่สร้างขึ้นจากคำสั่งสำหรับการเบิกวัตถุดิบควรถูกปัดเศษขึ้นเป็นตัวคูณของหนึ่งหน่วยจัดการวัสดุ ที่ระบุในหน้า **จำกัดตามหน่วย**

    > [!NOTE]
    > การตั้งค่า **ปัดเป็นหน่วย** นี้ จะใช้สำหรับชนิดใบสั่งงาน *การเบิกวัตถุดิบ* เท่านั้น และเฉพาะสำหรับคำสั่งสถานที่ที่ฟิลด์ **ชนิดงาน** ตั้งค่าเป็น *เบิกสินค้า* เท่านั้น

- **ระบุปริมาณการบรรจุ** –ถ้าคุณระบุปริมาณการบรรจุสำหรับใบสั่งขาย ใบสั่งโอนย้าย หรือใบสั่งผลิต กล่องการเครื่องหมายนี้จะช่วยให้คุณสามารถจำกัดระบบเพื่อให้สามารถเลือกเฉพาะสถานที่ที่มีปริมาณการบรรจุอย่างน้อย

    > [!NOTE]
    > ฟังก์ชันนี่จะใช้งานได้เฉพาะกับคำสั่งสถานที่สำหรับชนิดงาน *เบิกสินค้า*

- **อนุญาตให้แบ่ง** – ระบุว่าคำสั่งสถานที่ได้รับอนุญาตให้สามารถแบ่งปริมาณที่ได้รับ หรือปริมาณที่ถูกจองระหว่างคลังสินค้าหลายแห่ง หรือถ้าปริมาณสินค้าทั้งหมดต้องอยู่ในที่ตั้งเดียว หรือถูกจองจากสถานที่เดียวเพื่อ สร้างงาน
- **เทมเพลตการเติมสินค้าทันที** – ใช้ฟิลด์นี้เพื่อสร้างการเชื่อมต่อกับเทมเพลตการเติมสินค้าเพื่อให้การเติมสินค้าเริ่มต้นทันทีถ้าสินค้าไม่ได้รับการปันส่วน ถ้าคุณปล่อยฟิลด์นี้ว่างไว้ แสดงว่าการเติมสินค้าจะไม่เริ่มต้นจนกว่าจะมีการประมวลผลรายการทั้งหมดของคำสั่งสถานที่

    > [!NOTE]
    > ฟิลด์นี้จะพร้อมใช้งานสำหรับชนิดของใบสั่งงานที่เลือกเท่านั้นที่จะได้รับการเติมสินค้า สำหรับรายการทั้งหมด ให้ดูส่วน [ฟิลด์ที่ระบุให้กับชนิดของใบสั่งงาน](#fields-specific-types)

## <a name="location-directive-actions-fasttab"></a>ปุ่มด่วนการดำเนินการคำสั่งสถานที่

คุณสามารถกำหนดหลายการดำเนินคำสั่งสถานที่สำหรับแต่ละรายการ อีกครั้งหนึ่ง หมายเลขลำดับจะใช้เพื่อกำหนดลำดับที่การดำเนินการนั้นจะถูกประเมิน ในระดับนี้ คุณสามารถตั้งค่าคำสั่งเพื่อกำหนดวิธีเพื่อหาสถานที่ที่ดีที่สุดในคลังสินค้า คุณยังสามารถใช้ค่า **กลยุทธ์** ที่กำหนดไว้ล่วงหน้าเพื่อหาสถานที่ที่เหมาะสมได้

- **หมายเลขลำดับ** ฟิลด์นี้จะแสดงลำดับที่จะมีการดำเนินการสำหรับชนิดงานที่เลือก คุณสามารถเปลี่ยนลำดับได้โดยการใช้ปุ่ม **เลื่อนขึ้น** และ **เลื่อนลง** ในแถบเครื่องมือ
- **ชื่อ** - ป้อนชื่อสำหรับการดำเนินการคำสั่งของสถานที่ ระบุโดยเฉพาะ เพื่อให้การดำเนินการที่จะดำเนินการล้างข้อมูลจากชื่อ
- **การใช้สถานที่คงที่** – ระบุสถานที่ที่ควรพิจารณาคำสั่งสถานที่ เลือกค่าใดค่าหนึ่งต่อไปนี้

    - **สถานที่คงที่และไม่คงที่** - คำสั่งสถานที่จะพิจารณาสถานที่ทั้งหมด
    - **เฉพาะสถานที่คงที่สำหรับผลิตภัณฑ์** - คำสั่งสถานที่จะพิจารณาเฉพาะสถานที่คงที่สำหรับผลิตภัณฑ์นั้น
    - **เฉพาะสถานที่คงที่สำหรับผลิตภัณฑ์ย่อย** – คำสั่งสถานที่จะพิจารณาเฉพาะสถานที่คงที่สำหรับผลิตภัณฑ์ย่อย

- **อนุญาตสินค้าคงคลังค่าลบ** – เลือกกล่องการเครื่องหมายนี้เพื่ออนุญาตสินค้าคงคลังค่าลบในสถานที่คลังสินค้าคงคลังที่ระบุในคำสั่งสถานที่
- **ชุดงานที่เปิดใช้งาน** – เลือกกล่องกาเครื่องหมายนี้เพื่อใช้กลยุทธ์ชุดงานสำหรับสินค้าที่เปิดใช้งานชุดงาน คุณควรเลือกกล่องกาเครื่องหมายนี้สำหรับกระบวนการที่ใช้คำสั่งสถานที่ในการค้นหาที่ตั้งเพื่อเลือกหมายเลขชุดงาน–สินค้าที่ติดตาม การค้นหาสถานที่ที่มีหมายเลขชุดงานไว้–รวมถึงสินค้าที่ติดตาม ถ้าเลือกกล่องกาเครื่องหมายนี้ และฟิลด์ **กลยุทธ์** ตั้งค่าเป็น *ไม่มี* ระบบจะเลื่อนไปยังรายการการดำเนินการถัดไป
- **กลยุทธ์** –เพื่อให้ง่ายและเร็วมากขึ้นต่อการกำหนดการดำเนินการที่เชื่อมโยงกับแต่ละรายการคำสั่งที่ คุณสามารถเลือกกลยุทธ์กำหนดไว้ล่วงหน้าอย่างใดอย่างหนึ่งต่อไปนี้

    - **ไม่มี** – จะไม่มีการใช้กลยุทธ์
    - **จับคู่ปริมาณการบรรจุ** - กลยุทธ์นี้ตรวจสอบว่าสถานที่เบิกสินค้ามีปริมาณการบรรจุที่ระบุหรือไม่ กลยุทธ์นี้ใช้ได้เฉพาะเมื่อมีการตั้งค่าฟิลด์ **ชนิดงาน** เป็น *เบิกสินค้า* เท่านั้น
    - **รวมบัญชี** - กลยุทธ์นี้จะรวมสินค้าในสถานที่หนึ่งๆ เมื่อสินค้าที่คล้ายกันพร้อมใช้งานอยู่แล้ว กลยุทธ์นี้ใช้ได้เฉพาะเมื่อมีการตั้งค่าฟิลด์ **ชนิดงาน** เป็น *เก็บสินค้า* เท่านั้น การตั้งค่าทั่วไปสำหรับการเก็บสินค้าจะพยายามรวมบัญชีบนรายการการดำเนินการแรก ตามด้วยรายการที่สอง ซึ่งจะพยายามเก็บสินค้าโดยไม่มีการรวมบัญชี การรวมสินค้าทำให้การเบิกสินค้าในภายหลังในภายหลังมีประสิทธิภาพมากขึ้น
    - **การจองชุดงาน FEFO** – กลยุทธ์นี้ใช้การจองชุดงานที่หมดอายุก่อน ออกก่อน (FEFO) ใช้เมื่อตั้งอยู่โดยใช้วันหมดอายุของชุดงานสินค้าคงคลัง และมีการปันส่วนสำหรับการจองชุดงาน คุณสามารถใช้กลยุทธ์นี้สำหรับสินค้าที่เปิดใช้งานชุดงานเท่านั้น กลยุทธ์นี้ใช้ได้เฉพาะเมื่อมีการตั้งค่าฟิลด์ **ชนิดงาน** เป็น *เบิกสินค้า* เท่านั้น
    - **ปัดเศษขึ้นจนถึงชุดงานแบบ full LP และ FEFO** – กลยุทธ์นี้รวมองค์ประกอบของกลยุทธ์ *การจองชุดงาน FEFO* และ *ปัดเศษเป็น LP แบบเต็ม* มีผลบังคับใช้เฉพาะสำหรับสินค้าที่เปิดใช้งานชุดงานและคำสั่งสถานที่ที่มีชนิดงาน *การเบิกสินค้า* เท่านั้น รายการต้องมีการเปิดใช้งานชุดงานเพื่อใช้กลยุทธ์ *การจองชุดงาน FEFO* และกลยุทธ์ *การปัดเศษเป็นแบบ LP แบบเต็ม* สามารถใช้สำหรับการเพิ่มเติมสินค้าเท่านั้น ถ้ามีการตั้งค่าคอนฟิกกลยุทธ์นี้พร้อมกับขีดจำกัดของสถานที่เก็บ ซึ่งอาจทำให้สถานที่ทำงานการวางที่เลือกถูกข้ามไป และขีดจำกัดของการเก็บสต็อกเท่านั้นที่จะถูกละเว้น
    - **รวบรวมเป็นป้ายทะเบียนแบบเต็ม** - กลยุทธ์นี้จะใช้เพื่อปัดเศษปริมาณสินค้าคงคลังเพื่อให้ตรงกับปริมาณป้ายทะเบียนที่กำหนดให้กับสินค้าที่ต้องเบิก คุณสามารถใช้กลยุทธ์นี้ได้เฉพาะสำหรับคำสั่งสถานที่การเพิ่มเติมสินค้าของชนิด *การเบิกสินค้า* เท่านั้น ถ้ามีการตั้งค่าคอนฟิกกลยุทธ์นี้พร้อมกับขีดจำกัดของสถานที่เก็บ ซึ่งอาจทำให้สถานที่ทำงานการวางที่เลือกถูกข้ามไป และขีดจำกัดของการเก็บสต็อกเท่านั้นที่จะถูกละเว้น
    - **คำแนะนำป้ายทะเบียน** –ใช้กลยุทธ์นี้เมื่อคุณนำใบสั่งออกใช้ไปยังคลังสินค้าเพื่อสร้างงานการเบิกสินค้าและการรับสินค้า คุณสามารถใช้วิธีการนี้ได้สำหรับหลายป้ายทะเบียน กลยุทธ์นี้จะพยายามจอง และสร้างงานการเบิกสินค้ากับสถานที่เก็บป้ายทะเบียนที่ร้องขอที่เชื่อมโยงกับรายการใบสั่งโอนย้าย อย่างไรก็ตาม ถ้าไม่สามารถทำการดำเนินการเหล่านี้ให้เสร็จสมบูรณ์ได้ แต่คุณยังคงต้องการสร้างงานการเบิกสินค้า คุณควรถอยกลับไปยังอีกกลยุทธ์หนึ่งสำหรับการดำเนินการคำสั่งสถานที่ ทั้งนี้ขึ้นอยู่กับความต้องการของกระบวนการทางธุรกิจของคุณ คุณอาจต้องการค้นหาสินค้าคงคลังในอีกพื้นที่หนึ่งของคลังสินค้า
    - **ลบข้อมูลที่ตั้งโดยไม่มีงานขาเข้า** – ใช้กลยุทธ์นี้ในการระบุตำแหน่งที่ตั้งที่ว่างเปล่า สถานที่เก็บจะถือเป็นว่างเปล่าถ้ายังไม่มีสินค้าคงคลังทางกายภาพและไม่มีงานขาเข้าที่คาดไว้ คุณสามารถใช้กลยุทธ์นี้ได้เฉพาะสำหรับคำสั่งสถานที่ที่มีชนิดงานเป็น *ส่งสินค้า* เท่านั้น
    - **อายุหนี้ของสถานที่ FIFO** – ใช้กลยุทธ์เข้าก่อน ออกก่อน (FIFO) เพื่อจัดส่งทั้งสินค้าที่มีการติดตามชุดงานและสินค้าที่ไม่มีการติดตามชุดงาน โดยยึดตามวันที่ที่สินค้าคงคลังเข้าสู่คลังสินค้า ความสามารถนี้มีประโยชน์โดยเฉพาะอย่างยิ่งสำหรับสินค้าคงคลังที่ไม่มีการติดตามชุดงาน ซึ่งไม่มีวันหมดอายุที่พร้อมใช้งานสำหรับการเรียงลำดับ กลยุทธ์ FIFO ค้นหาสถานที่ที่มีวันที่อายุหนี้ที่เก่าที่สุด และจากนั้นจัดสรรการเบิกสินค้าตามวันที่อายุหนี้นั้น
    - **อายุหนี้ของสถานที่ LIFO** – ใช้กลยุทธ์เข้าหลัง ออกหลัง (LIFO) เพื่อจัดส่งทั้งสินค้าที่มีการติดตามชุดงานและสินค้าที่ไม่มีการติดตามชุดงาน โดยยึดตามวันที่ที่สินค้าคงคลังเข้าสู่คลังสินค้า ความสามารถนี้มีประโยชน์โดยเฉพาะอย่างยิ่งสำหรับสินค้าคงคลังที่ไม่มีการติดตามชุดงาน ซึ่งไม่มีวันหมดอายุที่พร้อมใช้งานสำหรับการเรียงลำดับ กลยุทธ์ LIFO ค้นหาสถานที่ที่มีวันที่อายุหนี้ที่ใหม่ที่สุด และจากนั้นจัดสรรการเบิกสินค้าตามวันที่อายุหนี้นั้น

## <a name="example-using-location-directives"></a>ตัวอย่าง: การใช้คำสั่งสถานที่

สำหรับตัวอย่างนี้ จะพิจารณากระบวนการใบสั่งซื้อที่ซึ่งคำสั่งสถานที่ต้องค้นหากำลังการผลิตที่ว่างอยู่ภายในคลังสินค้าสำหรับสินค้าคงคลังที่เพิ่งถูกลงทะเบียน ณ ท่าสินค้ารับสินค้า ก่อนอื่น คุณต้องค้นหากำลังการผลิตที่ว่างอยู่ภายในคลังสินค้าด้วยการรวมเข้ากับปริมาณสินค้าคงคลังคงเหลือที่มีอยู่ ถ้าไม่สามารถรวมได้ คุณจะต้องค้นหาสถานที่ที่ว่าง

สำหรับสถานการณ์จำลองนี้ คุณต้องกำหนดการดำเนินคำสั่งสถานที่สองรายการ การดำเนินการแรกในลำดับต้องใช้ยุทธ์ *รวม* และการดำเนินการที่สองควรใช้กลยุทธ์ *สถานที่ว่างโดยไม่มีงานขาเข้า* เว้นแต่ว่าคุณกำหนดการดำเนินการที่สามเพื่อจัดการสถานการณ์จำลองที่มากเกินไป ผลลัพธ์สองรายการอาจเป็นไปได้ เมื่อไม่มีกำลังการผลิตในคลังสินค้า: งานสามารถถูกสร้างได้ แม้ไม่มีการระบุสถานที่ หรือกระบวนการสร้างงานอาจล้มเหลวได้ ผลลัพธ์จะถูกกำหนดตามการตั้งค่าบนหน้า **คำสั่งสถานที่ล้มเหลว** ซึ่งคุณสามารถเลือกว่าจะเลิอก **หยุดงานเมื่อคำสั่งสถานที่ล้มเหลว** สำหรับแต่ละชนิดใบสั่งผลิตหรือไม่

## <a name="next-step"></a>ขั้นตอนต่อไป

หลังจากที่คุณสร้างคำสั่งสถานที่ คุณสามารถเชื่อมโยงแต่ละรหัสคำสั่งด้วยรหัสเทมเพลตงานสำหรับการสร้างงาน สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ควบคุมงานคลังสินค้าโดยใช้เทมเพลตงานและคำสั่งสถานที่](./control-warehouse-location-directives.md)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- วีดิโอ: [สำรวจดูรายละเอียดการตั้งค่าคอนฟิกการจัดการคลังสินค้า](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- บทความวิธีใช้: [ควบคุมงานคลังสินค้าโดยเทมเพลตงานและคำสั่งสถานที่](control-warehouse-location-directives.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
