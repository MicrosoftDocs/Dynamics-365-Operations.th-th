---
title: ตัวอย่างและตรรกะของรายงานมูลค่าของสินค้าคงคลัง
description: บทความนี้แสดงตัวอย่างผลลัพธ์ที่แสดงในรายงานมูลค่าสินค้าคงคลังแต่ละชนิด รายงานมูลค่าสินค้าคงคลังจะให้รายละเอียดเกี่ยวกับปริมาณและยอดเงินทางกายภาพและทางการเงินของสินค้าคงคลังของคุณ
author: JennySong-SH
ms.date: 10/19/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: e6c6387be5204fde6ebc7a4983567801900974af
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877666"
---
# <a name="inventory-value-report-examples-and-logic"></a>ตัวอย่างและตรรกะของรายงานมูลค่าของสินค้าคงคลัง

[!include [banner](../includes/banner.md)]

รายงานมูลค่าสินค้าคงคลังจะให้รายละเอียดเกี่ยวกับปริมาณและยอดเงินทางกายภาพและทางการเงินของสินค้าคงคลังของคุณ บทความนี้แสดงตัวอย่างผลลัพธ์ที่แสดงในรายงานมูลค่าสินค้าคงคลังแต่ละชนิด

หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีสร้างและใช้รายงานมูลค่าสินค้าคงคลังแต่ละชนิด โปรดดูที่ [รายงานมูลค่าสินค้าคงคลัง](inventory-value-report-storage.md)

## <a name="sample-data-that-is-used-in-these-examples"></a>ข้อมูลตัวอย่างที่ใช้ในตัวอย่างเหล่านี้

ตัวอย่างของบทความนี้จะขึ้นอยู่กับข้อมูลธุรกรรมสินค้าคงคลังตัวอย่างที่อธิบายไว้ในส่วนนี้

### <a name="storage-dimension-setup"></a>การตั้งค่ามิติการจัดเก็บ

ระบบตัวอย่างมีการตั้งค่าต่อไปนี้ของมิติการจัดเก็บ

| ชื่อ | ที่ใช้งานอยู่ | สินค้าคงคลังที่มีอยู่จริง | สินค้าคงคลังทางการเงิน |
|---|---|---|---|
| ไซต์ | ใช่ | ใช่ | ใช่ |
| คลังสินค้า | ใช่ | ใช่ | ไม่ |

### <a name="inventory-model"></a>แบบจำลองสินค้าคงคลัง

สำหรับระบบตัวอย่าง แบบจำลองสินค้าคงคลังสำหรับผลิตภัณฑ์ที่นำออกใช้คือ *FIFO* และฟิลด์ **ราคาต้นทุน** สำหรับแบบจำลองสินค้าคงคลังจะถูกกำหนดลงใน *รวมมูลค่าที่มีอยู่จริง*

### <a name="inventory-transactions"></a>ธุรกรรมสินค้าคงคลัง

ระบบตัวอย่างมีธุรกรรามของสินค้าคงคลังต่อไปนี้สำหรับผลิตภัณฑ์ที่นำออกใช้ที่มีหมายเลขสินค้า *B0001*

| อ้างอิง | ไซต์ | คลังสินค้า | ใบเสร็จรับเงิน | ปัญหา | วันที่ตามจริง | วันที่ทางการเงิน | ปริมาณ | จำนวนเงินต้นทุน | ยอดต้นทุนจริง |
|---|---|---|---|---|---|---|---|---|---|
| ใบสั่งซื้อ | 1 | 11 | ซื้อแล้ว | | 15 มีนาคม | 15 มีนาคม | 10 | 1,000 | 1,000 |
| ใบสั่งซื้อ | 2 | 21 | ซื้อแล้ว | | 15 มีนาคม | 15 มีนาคม | 10 | 2,000 | 2,000 |
| ใบสั่งซื้อ | 1 | 11 | ได้รับแล้ว | | 15 เมษายน | | 5 | | 375 |
| ใบสั่งโอน | 1 | 11 | | ขายแล้ว | พฤษภาคม 2 | พฤษภาคม 2 | -5 | -458.33 | -458.33 |
| ใบสั่งโอน | 1 | 12 | ซื้อแล้ว | | พฤษภาคม 2 | พฤษภาคม 2 | 5 | 458.33 | 458.33 |
| ใบสั่งขาย | 1 | 12 | | ขายแล้ว | พฤษภาคม 3 | พฤษภาคม 3 | -1 | -91.67 | -91.67 |

### <a name="inventory-value-report-configuration"></a>การตั้งค่าคอนฟิกรายงานมูลค่าสินค้าคงคลัง

ระบบตัวอย่างมีการตั้งค่าคอนฟิกรายงานมูลค่าสินค้าคงคลังซึ่งมีการตั้งค่าต่อไปนี้

- **ช่วง**  *วันที่ลงรายการบัญชี*
- **สินค้าคงคลัง** *ใช่*
- **คํานวณต้นทุนเฉลี่ยต่อหน่วย** *ใช่*
- **ปริมาณและมูลค่ารวม** *ใช่*
- **ไซต์, มุมมอง** *เลือก*
- **รหัสทรัพยากร, ดู** *ใช่*
- **ระดับ** *ผลรวม*

## <a name="inventory-value-report-example-1"></a>ตัวอย่างที่ 1 รายงานมูลค่าสินค้าคงคลัง

ตารางและภาพประกอบต่อไปนี้แสดงผลลัพธ์เมื่อคุณใช้ข้อมูลตัวอย่างและการตั้งค่าคอนฟิกรายงานที่อธิบายไว้ก่อนหน้านี้ในบทความนี้

| ชนิดทรัพยากร | ทรัพยากร | ไซต์ | ข้อมูลอ้างอิง | สินค้าคงคลัง: ปริมาณทางการเงิน | สินค้าคงคลัง: ยอดเงินทางการเงิน | สินค้าคงคลัง: ปริมาณที่มีอยู่จริงที่ลงรายการบัญชี | สินค้าคงคลัง: ยอดเงินจริงที่ลงรายการบัญชี | สินค้าคงคลัง: ปริมาณ | สินค้าคงคลัง: ยอดเงิน | ต้นทุนเฉลี่ยต่อหน่วย |
|---|---|---|---|---|---|---|---|---|---|---|
| วัสดุ | B0001 | 1 | ยอดดุลสิ้นงวด | 9.00 น. | 908.33 | 5.00 | 375.00 | 14.00 | 1,283.33 | 91.67 |
| วัสดุ | B0001 | 2 | ยอดดุลสิ้นงวด | 10.00 | 2,000.00 | 0.00 | 0.00 | 10.00 | 2,000.00 | 200.00 |

### <a name="standard-inventory-value-report-for-example-1"></a>สำหรับตัวอย่างที่ 1 รายงานการมูลค่าสินค้าคงคลังมาตรฐาน

สำหรับตัวอย่างที่ 1 ภาพประกอบต่อไปนี้แสดงรายงานมาตรฐาน **มูลค่าสินค้าคงคลัง** (เลือกภาพประกอบเพื่อเปิดเวอร์ชันที่ใหญ่ขึ้น)

[![สำหรับตัวอย่างที่ 1 รายงานการมูลค่าสินค้าคงคลัง](media/inventory-value-report-ex1-small.png "สำหรับตัวอย่างที่ 1 รายงานการมูลค่าสินค้าคงคลัง")](media/inventory-value-report-ex1.png)

### <a name="inventory-value-report-storage-report-for-example-1"></a>สำหรับตัวอย่างที่ 1 รายงานการจัดเก็บรายงานมูลค่าสินค้าคงคลัง

สำหรับตัวอย่างที่ 1 ภาพประกอบต่อไปนี้แสดงรายงาน **การจัดเก็บรายงานมูลค่าสินค้าคงคลัง** (เลือกภาพประกอบเพื่อเปิดเวอร์ชันที่ใหญ่ขึ้น)

[![สำหรับตัวอย่างที่ 1 รายงานการจัดเก็บรายงานมูลค่าสินค้าคงคลัง](media/inventory-value-report-storage-ex1-small.png "สำหรับตัวอย่างที่ 1 รายงานการจัดเก็บรายงานมูลค่าสินค้าคงคลัง")](media/inventory-value-report-storage-ex1.png)

## <a name="inventory-value-report-example-2"></a>ตัวอย่างที่ 2 รายงานมูลค่าสินค้าคงคลัง

ตารางและภาพประกอบต่อไปนี้จะแสดงผลลัพธ์เมื่อคุณใช้ข้อมูลตัวอย่างที่อธิบายไว้ก่อนหน้านี้ในบทความนี้ แต่คุณเปลี่ยนค่าของฟิลด์ **ระดับ** เป็น *ธุรกรรม* ในการตั้งค่าคอนฟิกรายงาน และตั้งค่าฟิลด์ **วันที่เริ่มต้น** เป็น *15 มีนาคม* เมื่อคุณรันรายงาน

| ชนิดทรัพยากร | ทรัพยากร | ไซต์ | วันที่ | ไม่ | อ้างอิง | สินค้าคงคลัง: ปริมาณทางการเงิน | สินค้าคงคลัง: ยอดเงินทางการเงิน | สินค้าคงคลัง: ปริมาณที่มีอยู่จริงที่ลงรายการบัญชี | สินค้าคงคลัง: ยอดเงินจริงที่ลงรายการบัญชี | สินค้าคงคลัง: ปริมาณ | สินค้าคงคลัง: ยอดเงิน |
|---|---|---|---|---|---|---|---|---|---|---|---|
| วัสดุ | B0001 | 1 | วันที่ 3/15/2021 | 00000126 | ใบสั่งซื้อ | 0.00 | 0.00 | 10.00 | 1,000.00 | **10.00** | **1,000.00** |
| วัสดุ | B0001 | 1 | วันที่ 3/15/2021 | 00000126 | ใบสั่งซื้อ | 10.00 | 1,000.00 | -10.00 | -1,000.00. | **0.00** | **0.00** |
| วัสดุ | B0001 | 1 | วันที่ 4/15/2021 | 00000128 | ใบสั่งซื้อ | 0.00 | 0.00 | 5.00 | 375.00 | **5.00** | **375.00** |
| วัสดุ | B0001 | 1 | วันที่ 5/2/2021 | 000003 | การจัดส่งตามใบสั่งโอนย้าย | -5.00. | -458.33 | 0.00 | 0.00 | **-5.00** | **-458.33** |
| วัสดุ | B0001 | 1 | วันที่ 5/2/2021 | 000003 | การรับสินค้าตามใบสั่งโอนย้าย | 5.00 | 458.33 | 0.00 | 0.00 | **5.00** | **458.33** |
| วัสดุ | B0001 | 1 | วันที่ 5/3/2021 | 000835 | ใบสั่งขาย | 0.00 | 0.00 | -1.00 | -91.67 | **-1.00** | **-91.67** |
| วัสดุ | B0001 | 1 | วันที่ 5/3/2021 | 000835 | ใบสั่งขาย | -1.00 | -91.67 | 1.00 | 91.67 | **0.00** | **0.00** |
| วัสดุ | B0001 | 2 | วันที่ 3/15/2021 | 00000127 | ใบสั่งซื้อ | 0.00 | 0.00 | 10.00 | 2,000.00 | **10.00** | **2,000.00** |
| วัสดุ | B0001 | 2 | วันที่ 3/15/2021 | 00000127 | ใบสั่งซื้อ | 10.00 | 2,000.00 | -10.00 | -2,000.00 | **0.00** | **0.00** |
| วัสดุ | B0001 | 2 | วันที่ 5/2/2021 | 000003 | การจัดส่งตามใบสั่งโอนย้าย | 5.00 | 458.33 | 0.00 | 0.00 | **5.00** | **458.33** |
| วัสดุ | B0001 | 2 | วันที่ 5/2/2021 | 000003 | การรับสินค้าตามใบสั่งโอนย้าย | -5.00. | -458.33 | 0.00 | 0.00 | **-5.00** | **-458.33** |

### <a name="standard-inventory-value-report-for-example-2"></a>สำหรับตัวอย่างที่ 2 รายงานการมูลค่าสินค้าคงคลังมาตรฐาน

สำหรับตัวอย่างที่ 2 ภาพประกอบต่อไปนี้แสดงรายงานมาตรฐาน **มูลค่าสินค้าคงคลัง** (เลือกภาพประกอบเพื่อเปิดเวอร์ชันที่ใหญ่ขึ้น)

[![สำหรับตัวอย่างที่ 2 รายงานการมูลค่าสินค้าคงคลัง](media/inventory-value-report-ex2-small.png "สำหรับตัวอย่างที่ 2 รายงานมูลค่าสินค้าคงคลัง")](media/inventory-value-report-ex2.png)

### <a name="inventory-value-report-storage-report-for-example-2"></a>สำหรับตัวอย่างที่ 2 รายงานการจัดเก็บรายงานมูลค่าสินค้าคงคลัง

สำหรับตัวอย่างที่ 2 ภาพประกอบต่อไปนี้แสดงรายงาน **การจัดเก็บรายงานมูลค่าสินค้าคงคลัง** (เลือกภาพประกอบเพื่อเปิดเวอร์ชันที่ใหญ่ขึ้น)

[![สำหรับตัวอย่างที่ 2 รายงานการจัดเก็บรายงานมูลค่าสินค้าคงคลัง](media/inventory-value-report-storage-ex2-small.png "สำหรับตัวอย่างที่ 2 รายงานการจัดเก็บรายงานมูลค่าสินค้าคงคลัง")](media/inventory-value-report-storage-ex2.png)

## <a name="inventory-value-report-example-3"></a>ตัวอย่างที่ 3 รายงานมูลค่าสินค้าคงคลัง

แนะนำให้คุณรันรายงานมูลค่าสินค้าคงคลังหลังจากการกระทบยอดใหม่หรือหลังการปิดบัญชีสินค้าคงคลัง เพื่อให้คุณมีธุรกรรมและยอดเงินที่ได้รับผลกระทบจากการกระทบยอดใหม่หรือการปิดบัญชีสินค้าคงคลัง

ส่วนย่อยต่อไปนี้แสดงรายงานมูลค่าสินค้าคงคลังที่สร้างขึ้นหลังจากที่คุณปิดบัญชีสินค้าคงคลังจนถึงวันที่ 30 พฤษภาคม

### <a name="example-3-when-the-totals-level-is-used"></a>ตัวอย่างที่ 3 เมื่อใช้ระดับผลรวม

ตารางต่อไปนี้แสดงผลลัพธ์เมื่อคุณใช้ข้อมูลตัวอย่างและการตั้งค่าคอนฟิกรายงานที่อธิบายไว้ก่อนหน้านี้ในบทความนี้ (ในการตั้งค่าคอนฟิกรายงานนั้น ฟิลด์ **ระดับ** ถูกตั้งค่าเป็น *ผลรวม*)

| ชนิดทรัพยากร | ทรัพยากร | ไซต์ | อ้างอิง | สินค้าคงคลัง: ปริมาณทางการเงิน | สินค้าคงคลัง: ยอดเงินทางการเงิน | สินค้าคงคลัง: ปริมาณที่มีอยู่จริงที่ลงรายการบัญชี | สินค้าคงคลัง: ยอดเงินจริงที่ลงรายการบัญชี | สินค้าคงคลัง: ปริมาณ | สินค้าคงคลัง: ยอดเงิน | ต้นทุนเฉลี่ยต่อหน่วย |
|---|---|---|---|---|---|---|---|---|---|---|
| วัสดุ | B0001 | 1 | ยอดดุลสิ้นงวด | 9.00 น. | 900.00 | 5.00 | 375.00 | 14.00 | 1,275.00 | 91.07 |
| วัสดุ | B0001 | 2 | ยอดดุลสิ้นงวด | 10.00 | 2,000.00 | 0.00 | 0.00 | 10.00 | 2,000.00 | 200.00 |

### <a name="example-3-when-the-transactions-level-is-used"></a>ตัวอย่างที่ 3 เมื่อใช้ระดับธุรกรรม

ตารางต่อไปนี้จะแสดงผลลัพธ์เมื่อคุณใช้ข้อมูลตัวอย่างที่อธิบายไว้ก่อนหน้านี้ในบทความนี้ แต่คุณเปลี่ยนค่าของฟิลด์ **ระดับ** เป็น *ธุรกรรม* ในการตั้งค่าคอนฟิกรายงาน

| ชนิดทรัพยากร | ทรัพยากร | ไซต์ | วันที่ | ไม่ | อ้างอิง | สินค้าคงคลัง: ปริมาณทางการเงิน | สินค้าคงคลัง: ยอดเงินทางการเงิน | สินค้าคงคลัง: ปริมาณที่มีอยู่จริงที่ลงรายการบัญชี | สินค้าคงคลัง: ยอดเงินจริงที่ลงรายการบัญชี | สินค้าคงคลัง: ปริมาณ | สินค้าคงคลัง: ยอดเงิน |
|---|---|---|---|---|---|---|---|---|---|---|---|
| วัสดุ | B0001 | 1 | วันที่ 3/15/2021 | 00000126 | ใบสั่งซื้อ | 0.00 | 0.00 | 10.00 | 1,000.00 | 10.00 | 1,000.00 |
| วัสดุ | B0001 | 1 | วันที่ 3/15/2021 | 00000126 | ใบสั่งซื้อ | 10.00 | 1,000.00 | -10.00 | -1,000.00. | 0.00 | 0.00 |
| วัสดุ | B0001 | 1 | วันที่ 4/15/2021 | 00000128 | ใบสั่งซื้อ | 0.00 | 0.00 | 5.00 | 375.00 | 5.00 | 375.00 |
| วัสดุ | B0001 | 1 | วันที่ 5/2/2021 | 000003 | การจัดส่งตามใบสั่งโอนย้าย | -5.00. | -458.33 | 0.00 | 0.00 | -5.00. | -458.33 |
| วัสดุ | B0001 | 1 | วันที่ 5/2/2021 | 000003 | การรับสินค้าตามใบสั่งโอนย้าย | 5.00 | 458.33 | 0.00 | 0.00 | 5.00 | 458.33 |
| วัสดุ | B0001 | 1 | วันที่ 5/3/2021 | 000835 | ใบสั่งขาย | 0.00 | 0.00 | -1.00 | -91.67 | -1.00 | -91.67 |
| วัสดุ | B0001 | 1 | วันที่ 5/3/2021 | 000835 | ใบสั่งขาย | -1.00 | -91.67 | 1.00 | 91.67 | 0.00 | 0.00 |
| วัสดุ | B0001 | 1 | วันที่ 5/31/2021 | 000835 | ใบสั่งขาย | 0.00 | -8.33 | 0.00 | 0.00 | 0.00 | -8.33 |
| วัสดุ | B0001 | 1 | วันที่ 5/31/2021 | 000003 | การจัดส่งตามใบสั่งโอนย้าย | 0.00 | -41.67 | 0.00 | 0.00 | 0.00 | -41.67 |
| วัสดุ | B0001 | 1 | วันที่ 5/31/2021 | 000003 | การรับสินค้าตามใบสั่งโอนย้าย | 0.00 | 41.67 | 0.00 | 0.00 | 0.00 | 41.67 |
| วัสดุ | B0001 | 2 | วันที่ 3/15/2021 | 00000127 | ใบสั่งซื้อ | 0.00 | 0.00 | 10.00 | 2,000.00 | 10.00 | 2,000.00 |
| วัสดุ | B0001 | 2 | วันที่ 3/15/2021 | 00000127 | ใบสั่งซื้อ | 10.00 | 2,000.00 | -10.00 | -2,000.00 | 0.00 | 0.00 |
| วัสดุ | B0001 | 2 | วันที่ 5/2/2021 | 000003 | การจัดส่งตามใบสั่งโอนย้าย | 5.00 | 458.33 | 0.00 | 0.00 | 5.00 | 458.33 |
| วัสดุ | B0001 | 2 | วันที่ 5/2/2021 | 000003 | การรับสินค้าตามใบสั่งโอนย้าย | -5.00. | -458.33 | 0.00 | 0.00 | -5.00. | -458.33 |
| วัสดุ | B0001 | 2 | วันที่ 5/31/2021 | 000003 | การจัดส่งตามใบสั่งโอนย้าย | 0.00 | 41.67 | 0.00 | 0.00 | 0.00 | 41.67 |
| วัสดุ | B0001 | 2 | วันที่ 5/31/2021 | 000003 | การรับสินค้าตามใบสั่งโอนย้าย | 0.00 | -41.67 | 0.00 | 0.00 | 0.00 | -41.67 |
