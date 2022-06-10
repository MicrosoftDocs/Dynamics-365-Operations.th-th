---
title: เอนทิตีการสร้างการเดินทาง
description: หัวข้อนี้มีข้อมูลเกี่ยวกับเอนทิตีข้อมูลการสร้างการเดินทาง ซึ่งจัดกลุ่มเอนทิตีข้อมูลที่ต้องใช้ในการสร้างการเดินทางในการทำงาน
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 17f63af3ce1f858ed3e2086fc81c5e17c5e76be0
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813134"
---
# <a name="voyage-creation-entities"></a>เอนทิตีการสร้างการเดินทาง

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

เอนทิตีข้อมูลการสร้างการเดินทางจัดกลุ่มเอนทิตีข้อมูลร่วมกันที่ต้องใช้ในการสร้างการเดินทางในการทำงาน คุณหรือผู้ขนส่งของคุณสามารถใช้เอนทิตีข้อมูลเหล่านี้เพื่อสร้างการเดินทาง คอนเทนเนอร์การจัดส่ง ใบแจ้งรายการ และเรกคอร์ดบรรทัดการเดินทางที่อ้างอิงใบสั่งซื้อหรือรายการใบสั่งโอนย้ายที่มีอยู่

## <a name="voyages-itmtableentity"></a>การเดินทาง (ITMTableEntity)

การเดินทางแสดงถึงการเดินทางของสินค้าขาเข้าและใช้เป็นพื้นที่ต้นทุนระดับสูงสุดในต้นทุนแฝง ซึ่งประกอบด้วยข้อมูลระดับหัวข้อที่เกี่ยวข้องกับเรือ ท่าเรือต้นทาง และท่าเรือปลายทาง ฟังก์ชันนี้รองรับโดยเอนทิตี `ITMTableEntity` ตารางต่อไปนี้แสดงรายการฟิลด์และการแม็ปที่เป็นของเอนทิตีนี้

| ชื่อ | การแม็ป | ชนิดข้อมูล | คีย์ | จำเป็น |
|---|---|---|---|---|
| วิธีการจัดส่ง | ITMTable.DlvModeId | Nvarchar(10) | ไม่ | ไม่ |
| นายหน้าแนะนำแล้ว | ITMTable.ITMBrokerAdvised | วันที่และเวลา | ไม่ | ไม่ |
| การนัดหมายลูกค้า | ITMTable.ITMCustomerAppointment | วันที่และเวลา | ไม่ | ไม่ |
| จัดส่งสินค้าที่คลังสินค้าแล้ว | ITMTable.ITMDelAtWarehouse | วันที่และเวลา | ไม่ | ไม่ |
| คำแนะนำในการจัดส่ง | ITMTable.ITMDeliveryInstructions | วันที่และเวลา | ไม่ | ไม่ |
| วันที่ออกเดินทาง | ITMTable.ITMDepartureDate | วันที่และเวลา | ไม่ | ไม่ |
| นำสินค้าออกใช้แล้ว | ITMTable.ITMGoodsReleased | วันที่และเวลา | ไม่ | ไม่ |
| วันที่ของการขนส่งท้องถิ่น | ITMTable.ITMLocalTransportDate | วันที่และเวลา | ไม่ | ไม่ |
| เวลาของการขนส่งท้องถิ่น | ITMTable.ITMLocalTransportTime | Int | ไม่ | ไม่ |
| ส่งต้นฉบับใบตราส่งแล้ว | ITMTable.ITMOriginalBOLSebt | วันที่และเวลา | ไม่ | ไม่ |
| ได้รับเอกสารต้นฉบับแล้ว | ITMTable.ITMOriginalDocsReceived | วันที่และเวลา | ไม่ | ไม่ |
| สถานะใบสั่งซื้อ | ITMTable.ITMPurchStatus | Int | ไม่ | ไม่ |
| วันที่ตรวจสอบความถูกต้อง | ITMTable.ITMVerificationDate | วันที่และเวลา | ไม่ | ไม่ |
| ตัวระบุรายการศุลกากร | ITMTable.ShipCustomsEntryId | Nvarchar(20) | ไม่ | ไม่ |
| วันที่จัดส่ง | ITMTable.ShipDate | วันที่และเวลา | ไม่ | ไม่ |
| คำอธิบาย | ITMTable.ShipDescription | Nvarchar(60) | ไม่ | ไม่ |
| เอกสารที่ได้รับ | ITMTable.ShipDocReceived | Int | ไม่ | ไม่ |
| วันที่จัดส่งโดยประมาณ | ITMTable.ShipEstDlvDate | วันที่และเวลา | ไม่ | ไม่ |
| ETA ที่ท่าเรือขนส่งสินค้า | ITMTable.ShipEstPortDate | วันที่และเวลา | ไม่ | ไม่ |
| จากท่าเรือ | ITMTable.ShipFromPort | Nvarchar(20) | ไม่ | ไม่ |
| ใบตราส่งสินค้าทางอากาศ/ใบตราส่ง | ITMTable.ShipHAWB | Nvarchar(20) | ไม่ | ไม่ |
| การเดินทาง | ITMTable.ShipId | Nvarchar(20) | **ใช่** | **ใช่** |
| การอ้างอิงการจอง | ITMTable.ShipIdExternal | Nvarchar(20) | ไม่ | ไม่ |
| เทมเพลตการเดินทาง | ITMTable.ShipJourneyId | Nvarchar(20) | ไม่ | ไม่ |
| ผู้ขนส่งสินค้าในท้องถิ่น | ITMTable.ShipLocalForwarder | Nvarchar(20) | ไม่ | ไม่ |
| ใบตราส่งสินค้าทางอากาศ/ใบตราส่งหลัก | ITMTable.ShipMAWB | Nvarchar(20) | ไม่ | ไม่ |
| การวัด | ITMTable.ShipMeasurement | Numeric(32, 6) | ไม่ | ไม่ |
| หน่วยการวัด | ITMTable.ShipMeasurementUnit | Int | ไม่ | ไม่ |
| จำนวนของแท่นวางสินค้า | ITMTable.ShipNoOfPallets | Int | ไม่ | ไม่ |
| การเดินทางที่ค้างอยู่ | ITMTable.ShipPending | Int | ไม่ | ไม่ |
| หมายเหตุ | ITMTable.ShipRemarks | Nvarchar(MAX) | ไม่ | ไม่ |
| การเช่า | ITMTable.ShipRental | Int | ไม่ | ไม่ |
| สถานะการเดินทาง | ITMTable.ShipStatusId | Nvarchar(20) | ไม่ | ไม่ |
| ปริมาณเป็นตัวเลข | ITMTable.ShipTallyInNumber | Nvarchar(20) | ไม่ | ไม่ |
| ไปยังท่าเรือ | ITMTable.ShipToPort | Nvarchar(20) | ไม่ | ไม่ |
| วันที่ประเมินค่า | ITMTable.ShipValuationDate | วันที่และเวลา | ไม่ | ไม่ |
| บริษัทจัดส่งสินค้า | ITMTable.ShipVendAccount | Nvarchar(20) | ไม่ | ไม่ |
| เรือ | ITMTable.ShipVesselId | Nvarchar(20) | ไม่ | **ใช่** |
| รหัสการเดินทางภายนอก | ITMTable.ShipVoyage | Nvarchar(20) | ไม่ | ไม่ |

### <a name="number-sequences-for-voyages"></a>ลำดับหมายเลขสำหรับการเดินทาง

ลำดับหมายเลขที่ใช้ร่วมกันสำหรับการเดินทางควบคุมการปันส่วนของรหัสการเดินทาง

ค่าที่ส่งผ่านไปยังเอนทิตีข้อมูลเป็นค่า **รหัสการเดินทาง** (`ShipId`) ใช้เพื่อระบุเรกคอร์ดที่มีอยู่เพื่ออัปเดต ถ้าไม่มีเรกคอร์ดดังกล่าวอยู่ ลักษณะการทำงานจะขึ้นอยู่กับว่าลำดับหมายเลขที่กําหนดไว้มีการตั้งค่าคอนฟิกไว้เพื่ออนุญาตให้ป้อนข้อมูลด้วยตนเองหรือไม่

- ถ้ามีการเปิดใช้งานการป้อนข้อมูลด้วยตนเอง เรกคอร์ดใหม่จะถูกสร้างขึ้นที่ใช้ค่าที่ผ่าน
- ถ้าไม่ได้เปิดใช้งานการป้อนข้อมูลด้วยตนเอง ระบบจะใช้หมายเลขถัดไปในลำดับหมายเลขที่มอบหมายแทนค่าที่ผ่าน

ในระหว่างรอบเวลาการนําเข้า ค่าตัวยึดสิทธิ์ที่นําเข้าเป็นรหัสการเดินทางจะถูกรักษาไว้ ลักษณะการทำงานนี้ช่วยให้มั่นใจว่าคอนเทนเนอร์และรายการการเดินทางที่อ้างอิงตัวยึดจะรวมอยู่ในการเดินทาง และจะมีการอัปเดตเพื่อสะท้อนค่าที่มอบหมายจากลำดับหมายเลข

### <a name="automatic-cost-transactions"></a>ธุรกรรมต้นทุนอัตโนมัติ

คุณสามารถเพิ่มต้นทุนอัตโนมัติเข้าในการเดินทางได้จากหน้า **ต้นทุนอัตโนมัติ** ใน Microsoft Dynamics 365 Supply Chain Management (**ต้นทุนแฝง \> การตั้งค่าการคิดต้นทุน \> ต้นทุนอัตโนมัติ**) เรกคอร์ดของต้นทุนอัตโนมัติยังสามารถสร้างขึ้นได้โดยใช้เอนทิตีข้อมูลธุรกรรมต้นทุนของพื้นที่ต้นทุนแต่ละพื้นที่ที่ต้นทุนแฝงสนับสนุน

ต้นทุนอัตโนมัติที่ตั้งค่าคอนฟิกใน Supply Chain Management จะใช้ได้กับการเดินทางเมื่อสร้างรายการการเดินทาง ไม่มีต้นทุนที่มองเห็นได้กับเรกคอร์ดจนกว่าจะมีการเชื่อมโยงเรกคอร์ดหัวข้อกับข้อมูลรายการ

## <a name="shipping-containers-itmcontainersentity"></a>คอนเทนเนอร์การจัดส่ง (ITMContainersEntity)

คอนเทนเนอร์การจัดส่งแสดงถึงคอนเทนเนอร์ทางกายภาพที่มีการขนส่งสินค้า คอนเทนเนอร์ทางกายภาพนี้อาจเป็นคอนเทนเนอร์การขนส่งทางเรือหรือแท่นวางสินค้าเดียวที่สามารถขนส่งทางอากาศได้ คอนเทนเนอร์การจัดส่งประกอบด้วยข้อมูลระดับหัวข้อที่เกี่ยวข้องกับรหัสคอนเทนเนอร์ หมายเลขตราประทับ และชนิดคอนเทนเนอร์การจัดส่ง (ชนิดคอนเทนเนอร์การจัดส่งจะให้ข้อมูลมิติ) ฟังก์ชันนี้สนับสนุนโดยเอนทิตี `ITMContainersEntity` ตารางต่อไปนี้แสดงรายการฟิลด์และการแม็ปที่เป็นของเอนทิตีนี้

| ชื่อ | การแม็ป | ชนิดข้อมูล | คีย์ | จำเป็น |
|---|---|---|---|---|
| วันที่ออกเดินทาง | ITMContainers.ITMDepartureDate | วันที่และเวลา | ไม่ | ไม่ |
| วันที่ของการขนส่งท้องถิ่น | ITMContainers.ITMLocalTransportDate | วันที่และเวลา | ไม่ | ไม่ |
| เวลาของการขนส่งท้องถิ่น | ITMContainers.ITMLocalTransportTime | Int | ไม่ | ไม่ |
| การเดินทางเดิม | ITMContainers.OrigShipId | Nvarchar(20) | ไม่ | ไม่ |
| น้ำหนักจริง | ITMContainers.ShipActualWeight | Numeric(32, 6) | ไม่ | ไม่ |
| นายหน้าแนะนำแล้ว | ITMContainers.ShipBrokerAdvised | วันที่และเวลา | ไม่ | ไม่ |
| คอนเทนเนอร์การจัดส่ง | ITMContainers.ShipContainerId | Nvarchar(20) | **ใช่** | **ใช่** |
| ชนิดคอนเทนเนอร์การจัดส่ง | ITMContainers.ShipContainerTypeId | Nvarchar(20) | ไม่ | ไม่ |
| ชนิดของหน่วย | ITMContainers.ShipContainerUnitTypeId | Nvarchar(10) | ไม่ | ไม่ |
| แปลงเป็นแบบเช่าแล้ว | ITMContainers.ShipConvertedToRental | Int | ไม่ | ไม่ |
| การนัดหมายลูกค้า | ITMContainers.ShipCustomerAppointment | วันที่และเวลา | ไม่ | ไม่ |
| วันที่จัดส่ง | ITMContainers.ShipDate | วันที่และเวลา | ไม่ | ไม่ |
| จัดส่งสินค้าที่คลังสินค้าแล้ว | ITMContainers.ShipDelAtWarehouse | วันที่และเวลา | ไม่ | ไม่ |
| คำแนะนำในการจัดส่ง | ITMContainers.ShipDeliveryInstructions | วันที่และเวลา | ไม่ | ไม่ |
| วันที่ใช้ใบรับรองการสอบ | ITMContainers.ShipECAppliedDate | วันที่และเวลา | ไม่ | ไม่ |
| วันหมดอายุของใบรับรองการสอบ | ITMContainers.ShipECExpiryDate | วันที่และเวลา | ไม่ | ไม่ |
| หมายเลขใบรับรองการสอบ | ITMContainers.ShipECNum | Nvarchar(20) | ไม่ | ไม่ |
| วันที่ได้รับใบรับรองการสอบ | ITMContainers.ShipECReceivedDate | วันที่และเวลา | ไม่ | ไม่ |
| วันที่จัดส่งโดยประมาณ | ITMContainers.ShipEstDlvDate | วันที่และเวลา | ไม่ | ไม่ |
| ETA ที่ท่าเรือขนส่งสินค้า | ITMContainers.ShipEstPortDate | วันที่และเวลา | ไม่ | ไม่ |
| วันที่โหลดที่คาดไว้ | ITMContainers.ShipExpectedLoadingDate | วันที่และเวลา | ไม่ | ไม่ |
| จากท่าเรือ | ITMContainers.ShipFromPort | Nvarchar(20) | ไม่ | ไม่ |
| คำอธิบายเกี่ยวกับสินค้า | ITMContainers.ShipGoodsDesc | Nvarchar(60) | ไม่ | ไม่ |
| นำสินค้าออกใช้แล้ว | ITMContainers.ShipGoodsReleased | วันที่และเวลา | ไม่ | ไม่ |
| หน่วยตัวติดตาม GPS | ITMContainers.ShipGPSUnit | Nvarchar(30) | ไม่ | ไม่ |
| ใบตราส่งสินค้าทางอากาศ/ใบตราส่ง | ITMContainers.ShipHAWB | Nvarchar(20) | ไม่ | ไม่ |
| การเดินทาง | ITMContainers.ShipId | Nvarchar(20) | **ใช่** | **ใช่** |
| เทมเพลตการเดินทาง | ITMContainers.ShipJourneyId | Nvarchar(20) | ไม่ | ไม่ |
| ผู้ขนส่งสินค้าในท้องถิ่น | ITMContainers.ShipLocalForwarder | Nvarchar(20) | ไม่ | ไม่ |
| การวัด | ITMContainers.ShipMeasurement | Numeric(32, 6) | ไม่ | ไม่ |
| หน่วยการวัด | ITMContainers.ShipMeasurementUnit | Int | ไม่ | ไม่ |
| จำนวนกล่อง | ITMContainers.ShipNoOfCartons | Numeric(32, 6) | ไม่ | ไม่ |
| ส่งต้นฉบับใบตราส่งแล้ว | ITMContainers.ShipOriginalBOLSebt | วันที่และเวลา | ไม่ | ไม่ |
| ได้รับเอกสารต้นฉบับแล้ว | ITMContainers.ShipOriginalDocsReceived | วันที่และเวลา | ไม่ | ไม่ |
| หมายเลขตราประทับของเรา | ITMContainers.ShipOurSealNum | Nvarchar(20) | ไม่ | ไม่ |
| ใช้แล้ว | ITMContainers.ShipPendingUsed | Int | ไม่ | ไม่ |
| สถานะใบสั่งซื้อ | ITMContainers.ShipPurchStatus | Int | ไม่ | ไม่ |
| ชนิดการทำความเย็น | ITMContainers.ShipRefrigerationTypeId | Nvarchar(10) | ไม่ | ไม่ |
| หมายเหตุ | ITMContainers.ShipRemarks | Nvarchar(MAX) | ไม่ | ไม่ |
| การเช่า | ITMContainers.ShipRental | Int | ไม่ | ไม่ |
| ส่งคืนได้ | ITMContainers.ShipReturnable | Int | ไม่ | ไม่ |
| สถานะการเดินทาง | ITMContainers.ShipStatusId | Nvarchar(20) | ไม่ | ไม่ |
| หมายเลขตราประทับของบริษัทจัดส่งสินค้า | ITMContainers.ShipTheirSealNum | Nvarchar(20) | ไม่ | ไม่ |
| ไปยังท่าเรือ | ITMContainers.ShipToPort | Nvarchar(20) | ไม่ | ไม่ |
| วันที่ตรวจสอบความถูกต้อง | ITMContainers.ShipVerificationDate | วันที่และเวลา | ไม่ | ไม่ |
| เรือ | ITMContainers.ShipVesselId | Nvarchar(20) | ไม่ | **ใช่** |

### <a name="voyage-id-validation"></a>การตรวจสอบความถูกต้องรหัสการเดินทาง

รหัสคอนเทนเนอร์การจัดส่งไม่ได้ควบคุมโดยลำดับหมายเลข ซึ่งมีเอกลักษณ์เฉพาะในบริบทของการเดินทางที่ใช้อยู่เท่านั้น

ถ้าเอนทิตีคอนเทนเนอร์ (`ITMContainersEntity`) ถูกใช้อย่างเป็นอิสระจากเอนทิตีการเดินทาง (`ITMTableEntity`) ค่า **รหัสการเดินทาง** (`ShipId`) ต้องตรงกับเรกคอร์ดที่มีอยู่ในตารางการเดินทาง ไม่เช่นนั้น การนําเข้าจะล้มเหลว

หากเอนทิตีคอนเทนเนอร์การจัดส่ง (`ITMContainersEntity`) และเอนทิตีการเดินทาง (`ITMTableEntity`) ใช้เป็นส่วนหนึ่งของรอบเวลาการนําเข้าเดียวกัน เอนทิตีการเดินทางต้องนําหน้าการสร้างคอนเทนเนอร์การจัดส่ง มิฉะนั้น ค่า **รหัสการเดินทาง** (`ShipId`) จะตรวจสอบความถูกต้องไม่ได้ หากมีการใช้ค่าตัวยึด **รหัสการเดินทาง** (`ShipId`) การเชื่อมโยงสามารถสร้างได้ก็ต่อเมื่อใช้ตัวยึดตัวเดียวกันกับค่า **รหัสการเดินทาง** (`ShipId`) ในเอนทิตีคอนเทนเนอร์การจัดส่ง

### <a name="other-field-validations"></a>การตรวจสอบความถูกต้องฟิลด์อื่น

ตารางต่อไปนี้แสดงฟิลด์ในตารางคอนเทนเนอร์การจัดส่ง (`ITMContainers`) ที่จะตรวจสอบความถูกต้องกับตารางการตั้งค่าต้นทุนแฝง และยังแสดงเอนทิตีข้อมูลต้นทุนขแฝงที่ผู้ขนส่งสามารถใช้เพื่ออ่านค่าที่มีอยู่ และตรวจสอบให้แน่ใจว่าได้รับค่าที่ถูกต้องในสภาพแวดล้อมของคุณ

| ฟิลด์ในตาราง ITMContainers | เอนทิตีข้อมูลต้นทุนแฝง |
|---|---|
| ชนิดคอนเทนเนอร์การจัดส่ง | ITMShippingContainerTypeEntity |
| คำอธิบายเกี่ยวกับสินค้า | ITMGoodsDescriptionEntity |
| ชนิดการทำความเย็น | ITMShippingContainerRefrigerationTypeEntity |

## <a name="folios-itmfolioentity"></a>ใบแจ้งรายการ (ITMFolioEntity)

ใบแจ้งรายการนี้แสดงถึงการจัดกลุ่มสินค้าในคอนเทนเนอร์การจัดส่งเพื่อวัตถุประสงค์ในการรายงานภาษีศุลกากร ใบแจ้งรายการมีข้อมูลระดับหัวข้อที่เกี่ยวข้องกับนายหน้าศุลกากรและคำอธิบายเกี่ยวกับสินค้า ฟังก์ชันนี้รองรับโดยเอนทิตี `ITMFolioEntity` ตารางต่อไปนี้แสดงรายการฟิลด์และการแม็ปที่เป็นของเอนทิตีนี้

| ชื่อ | การแม็ป | ชนิดข้อมูล | คีย์ | จำเป็น |
|---|---|---|---|---|
| นายหน้าแนะนำแล้ว | ITMFolioTable.ShipBrokerAdvised | วันที่และเวลา | ไม่ | ไม่ |
| หมายเลขควบคุมการขนส่งสินค้า | ITMFolioTable.ShipCargoControlNumber | Nvarchar(20) | ไม่ | ไม่ |
| การนัดหมายลูกค้า | ITMFolioTable.ShipCustomerAppointment | วันที่และเวลา | ไม่ | ไม่ |
| นายหน้าศุลกากร | ITMFolioTable.ShipCustomsBroker | Nvarchar(20) | ไม่ | ไม่ |
| รหัสศุลกากร | ITMFolioTable.ShipCustomsId | Nvarchar(60) | ไม่ | ไม่ |
| บริษัท | ITMFolioTable.ShipDataArea | Nvarchar(4) | ไม่ | **ใช่** |
| จัดส่งสินค้าที่คลังสินค้าแล้ว | ITMFolioTable.ShipDelAtWarehouse | วันที่และเวลา | ไม่ | ไม่ |
| คำแนะนำในการจัดส่ง | ITMFolioTable.ShipDeliveryInstructions | วันที่และเวลา | ไม่ | ไม่ |
| เอกสารที่ได้รับ | ITMFolioTable.ShipDocReceived | Int | ไม่ | ไม่ |
| วันที่จัดส่งโดยประมาณ | ITMFolioTable.ShipEstDlvDate | วันที่และเวลา | ไม่ | ไม่ |
| ETA ที่ท่าเรือขนส่งสินค้า | ITMFolioTable.ShipEstPortDate | วันที่และเวลา | ไม่ | ไม่ |
| ผู้ส่งออก | ITMFolioTable.ShipExporterId | Nvarchar(20) | ไม่ | ไม่ |
| ชื่อ | ITMFolioTable.ShipExporterName | Nvarchar(60) | ไม่ | ไม่ |
| วันที่ใบแจ้งรายการ | ITMFolioTable.ShipFolioDate | วันที่และเวลา | ไม่ | ไม่ |
| ใบแจ้งรายการ | ITMFolioTable.ShipFolioId | Nvarchar(20) | **ใช่** | **ใช่** |
| จากท่าเรือ | ITMFolioTable.ShipFromPort | Nvarchar(20) | ไม่ | ไม่ |
| คำอธิบายเกี่ยวกับสินค้า | ITMFolioTable.ShipGoodsDesc | Nvarchar(60) | ไม่ | ไม่ |
| นำสินค้าออกใช้แล้ว | ITMFolioTable.ShipGoodsReleased | วันที่และเวลา | ไม่ | ไม่ |
| ใบตราส่งสินค้าทางอากาศ/ใบตราส่ง | ITMFolioTable.ShipHAWB | Nvarchar(20) | ไม่ | ไม่ |
| การเดินทาง | ITMFolioTable.ShipId | Nvarchar(20) | ไม่ | **ใช่** |
| การวัด | ITMFolioTable.ShipMeasurement | Numeric(32, 6) | ไม่ | ไม่ |
| หน่วยการวัด | ITMFolioTable.ShipMeasurementUnit | Int | ไม่ | ไม่ |
| จำนวนกล่อง | ITMFolioTable.ShipNoOfCartons | Numeric(32, 6) | ไม่ | ไม่ |
| ส่งต้นฉบับใบตราส่งแล้ว | ITMFolioTable.ShipOriginalBOLSebt | วันที่และเวลา | ไม่ | ไม่ |
| ได้รับเอกสารต้นฉบับแล้ว | ITMFolioTable.ShipOriginalDocsReceived | วันที่และเวลา | ไม่ | ไม่ |
| สถานะใบสั่งซื้อ | ITMFolioTable.ShipPurchStatus | Int | ไม่ | ไม่ |
| หมายเหตุ | ITMFolioTable.ShipRemarks | Nvarchar(MAX) | ไม่ | ไม่ |
| สถานะการเดินทาง | ITMFolioTable.ShipStatusId | Nvarchar(20) | ไม่ | ไม่ |
| รหัสภาษี | ITMFolioTable.ShipTariffCode | Nvarchar(10) | ไม่ | ไม่ |
| ไปยังท่าเรือ | ITMFolioTable.ShipToPort | Nvarchar(20) | ไม่ | ไม่ |
| วันที่ประเมินค่า | ITMFolioTable.ShipValuationDate | วันที่และเวลา | ไม่ | ไม่ |
| วันที่ตรวจสอบความถูกต้อง | ITMFolioTable.ShipVerificationDate | วันที่และเวลา | ไม่ | ไม่ |
| บัญชีผู้จัดจำหน่าย | ITMFolioTable.VendAccount | Nvarchar(20) | ไม่ | ไม่ |

### <a name="number-sequences-for-folios"></a>ลำดับหมายเลขสำหรับใบแจ้งรายการ

ลำดับหมายเลขสำหรับใบแจ้งรายการควบคุมการปันส่วนของรหัสใบแจ้งรายการ

ค่าที่ส่งผ่านไปยังเอนทิตีข้อมูลเป็นค่า **รหัสใบแจ้งรายการ** (`FolioId`) ใช้เพื่อระบุเรกคอร์ดที่มีอยู่เพื่ออัปเดต ถ้าไม่มีเรกคอร์ดดังกล่าวอยู่ ลักษณะการทำงานจะขึ้นอยู่กับว่าลำดับหมายเลขที่กําหนดไว้มีการตั้งค่าคอนฟิกไว้เพื่ออนุญาตให้ป้อนข้อมูลด้วยตนเองหรือไม่

- ถ้ามีการเปิดใช้งานการป้อนข้อมูลด้วยตนเอง เรกคอร์ดใหม่จะถูกสร้างขึ้นที่ใช้ค่าที่ผ่าน
- ถ้าไม่ได้เปิดใช้งานการป้อนข้อมูลด้วยตนเอง ระบบจะใช้หมายเลขถัดไปในลำดับหมายเลขที่มอบหมายแทนค่าที่ผ่าน

ในระหว่างรอบเวลาการนําเข้า ค่าตัวยึดสิทธิ์ที่นําเข้าเป็นรหัสใบแจ้งรายการจะถูกรักษาไว้ ลักษณะการทำงานนี้ช่วยให้มั่นใจว่ารายการการเดินทางที่อ้างอิงตัวยึดเชื่อมโยงอย่างถูกต้อง และจะมีการอัปเดตเพื่อสะท้อนค่าที่มอบหมายจากลำดับหมายเลข

### <a name="field-validations"></a>การตรวจสอบความถูกต้องของฟิลด์

ฟิลด์ **คำอธิบายสินค้า** ในตารางใบแจ้งรายการ (`ITMFolioTable`) จะมีการตรวจสอบความถูกต้องโดยเทียบกับตารางการตั้งค่าต้นทุนแฝงของชื่อเดียวกัน ผู้ขนส่งสามารถใช้เอนทิตีข้อมูลต้นทุนแฝง `ITMGoodsDescriptionEntity` เพื่ออ่านค่าที่มีอยู่ และตรวจสอบให้แน่ใจว่าได้รับค่าที่ถูกต้องในสภาพแวดล้อมของคุณ

## <a name="voyage-lines-for-purchase-orders-itmpurchaselineentity"></a>รายการการเดินทางในใบสั่งซื้อ (ITMPurchaseLineEntity)

รายการการเดินทางแสดงถึงรายการใบสั่งซื้อรายการเดียวซึ่งรวมอยู่ในการเดินทาง ความสัมพันธ์นี้มีการสร้างโดยใช้ฟิลด์ **หมายเลขใบสั่งซื้อ** และ **หมายเลขรายการซื้อ** บรรทัดการเดินทางจะอ้างอิงเรกคอร์ดก่อนหน้านี้แต่ละเรกคอร์ดที่สร้างขึ้นเพื่อการเดินทาง คอนเทนเนอร์ขนส่ง การจัดส่ง และใบแจ้งรายการ ฟังก์ชันนี้รองรับโดยเอนทิตี `ITMPurchaseLineEntity` ตารางต่อไปนี้แสดงรายการฟิลด์และการแม็ปที่เป็นของเอนทิตีนี้

| ชื่อ | การแม็ป | ชนิดข้อมูล | คีย์ | จำเป็น |
|---|---|---|---|---|
| สกุลเงิน | ITMLine.CurrencyCode | Nvarchar(3) | ไม่ | ไม่ |
| ยอดเงินสุทธิ | ITMLine.LineAmountMST | Numeric(32, 6) | ไม่ | ไม่ |
| หมายเลขรายการการซื้อ | ITMLine.RefRecId | Numeric(32, 6) | **ใช่** | ไม่ |
| คอนเทนเนอร์การจัดส่ง | ITMLine.ShipContainerId | Int | ไม่ | ไม่ |
| บริษัท | ITMLine.ShipDataArea | Nvarchar(20) | **ใช่** | ไม่ |
| ปริมาณที่ประกาศ | ITMLine.ShipDeclaredQty | Nvarchar(4) | ไม่ | ไม่ |
| ใบแจ้งรายการ | ITMLine.ShipFolioId | Numeric(32, 6) | ไม่ | ไม่ |
| การเดินทาง | ITMLine.ShipId | Nvarchar(20) | **ใช่** | ไม่ |
| หมายเลขสินค้า | ITMLine.ShipItemId | Nvarchar(20) | ไม่ | ไม่ |
| การวัด | ITMLine.ShipMeasurement | Nvarchar(20) | ไม่ | ไม่ |
| หน่วยการวัด | ITMLine.ShipMeasurementUnit | Numeric(32, 6) | ไม่ | ไม่ |
| จำนวนกล่อง | ITMLine.ShipNoOfCartons | Int | ไม่ | ไม่ |
| ตำแหน่ง | ITMLine.ShipPosition | Numeric(32, 6) | ไม่ | ไม่ |
| ปริมาณ | ITMLine.ShipQty | Int | ไม่ | ไม่ |
| หมายเลขใบสั่งซื้อ | ITMLine.TransRefId | Numeric(32, 6) | **ใช่** | ไม่ |
| หน่วย | ITMLine.UnitId | Int | ไม่ | ไม่ |
| ระดับเสียง | ITMLine.Volume | Nvarchar(10) | ไม่ | ไม่ |
| น้ำหนัก | ITMLine.Weight | Numeric(32, 6) | ไม่ | ไม่ |

## <a name="voyage-lines-for-transfer-orders-itmtransferlineentity"></a>รายการการเดินทางในใบสั่งโอนย้าย (ITMTransferLineEntity)

รายการการเดินทางแสดงถึงรายการใบสั่งโอนย้ายรายการเดียวซึ่งรวมอยู่ในการเดินทาง ความสัมพันธ์นี้มีการสร้างโดยใช้ฟิลด์ **หมายเลขใบสั่งโอนย้าย** และ **หมายเลขรายการโอนย้าย** บรรทัดการเดินทางจะอ้างอิงเรกคอร์ดก่อนหน้านี้แต่ละเรกคอร์ดที่สร้างขึ้นเพื่อการเดินทาง คอนเทนเนอร์ขนส่ง การจัดส่ง และใบแจ้งรายการ ฟังก์ชันนี้รองรับโดยเอนทิตี `ITMTransferLineEntity` ตารางต่อไปนี้แสดงรายการฟิลด์และการแม็ปที่เป็นของเอนทิตีนี้

| ชื่อ | การแม็ป | ชนิดข้อมูล | คีย์ | จำเป็น |
|---|---|---|---|---|
| สกุลเงิน | ITMLine.CurrencyCode | Nvarchar(3) | ไม่ | ไม่ |
| ยอดเงินสุทธิ | ITMLine.LineAmountMST | Numeric(32, 6) | ไม่ | ไม่ |
| คอนเทนเนอร์การจัดส่ง | ITMLine.ShipContainerId | Int | ไม่ | ไม่ |
| บริษัท | ITMLine.ShipDataArea | Nvarchar(20) | **ใช่** | ไม่ |
| ปริมาณที่ประกาศ | ITMLine.ShipDeclaredQty | Nvarchar(4) | ไม่ | ไม่ |
| ใบแจ้งรายการ | ITMLine.ShipFolioId | Numeric(32, 6) | ไม่ | ไม่ |
| การเดินทาง | ITMLine.ShipId | Nvarchar(20) | **ใช่** | ไม่ |
| หมายเลขสินค้า | ITMLine.ShipItemId | Nvarchar(20) | ไม่ | ไม่ |
| การวัด | ITMLine.ShipMeasurement | Nvarchar(20) | ไม่ | ไม่ |
| หน่วยการวัด | ITMLine.ShipMeasurementUnit | Numeric(32, 6) | ไม่ | ไม่ |
| จำนวนกล่อง | ITMLine.ShipNoOfCartons | Int | ไม่ | ไม่ |
| ตำแหน่ง | ITMLine.ShipPosition | Numeric(32, 6) | ไม่ | ไม่ |
| ปริมาณ | ITMLine.ShipQty | Int | ไม่ | ไม่ |
| หมายเลขรายการการโอน | ITMLine.TransferLineNumber | Numeric(32, 6) | **ใช่** | ไม่ |
| หมายเลขใบสั่งโอนย้าย | ITMLine.TransRefId | Numeric(32, 6) | **ใช่** | ไม่ |
| หน่วย | ITMLine.UnitId | Int | ไม่ | ไม่ |
| ระดับเสียง | ITMLine.Volume | Nvarchar(10) | ไม่ | ไม่ |
| น้ำหนัก | ITMLine.Weight | Numeric(32, 6) | ไม่ | ไม่ |

### <a name="reference-table"></a>ตารางอ้างอิง

รายการการเดินทางสร้างขึ้นผ่านการเชื่อมโยงกับรายการใบสั่งขาเข้าที่เปิด บรรทัดนี้สามารถอยู่ในใบสั่งซื้อ หรืออาจเป็นธุรกรรมการรับสินค้าในใบสั่งโอนย้าย ฟิลด์ `RefTableId` ในตารางรายการการเดินทาง (`ITMLine`) จะระบุชนิดใบสั่งที่บรรทัดนั้นเกี่ยวข้องด้วยการอ้างอิงหมายเลขตาราง หากมีการอ้างอิงหมายเลขตารางเฉพาะในตารางที่มีการสร้างข้อมูล เอนทิตีจะถูกแบ่งตามค่าเหล่านั้น

ค่าสำหรับตารางอ้างอิง (`RefTableId`) และชนิดธุรกรรม (`TransType`) จะเป็นแบบโดยนัยในการเลือกเอนทิตีรายการซื้อของต้นทุนแฝงหรือเอนทิตีรายการโอนย้ายต้นทุนแฝง

### <a name="validation"></a>การตรวจสอบความถูกต้อง

บรรทัดการเดินทางจะอ้างอิงเรกคอร์ดการเดินทาง เรกคอร์ดคอนเทนเนอร์การจัดส่ง และเรกคอร์ดใบแจ้งรายการโดยตรง ถ้าเอนทิตีรายการซื้อ (`ITMPurchaseLinesEntity`) หรือเอนทิตีรายการโอนย้าย (`ITMPurchaseLinesEntity`) ใช้อย่างอิสระจากเอนทิตีที่ใช้เพื่อสร้างเรกคอร์ดอ้างอิงเหล่านี้ ค่า **รหัสการเดินทาง** (`ShipId`), **คอนเทนเนอร์การจัดส่ง** (`ShipContainerId`) และ **ใบแจ้งรายการ** (`ShipFolioId`) ต้องตรงกับเรกคอร์ดที่มีอยู่ในตารางที่เกี่ยวข้อง ไม่เช่นนั้น การนําเข้าจะล้มเหลว

หากมีการใช้เอนทิตีรายการเป็นส่วนหนึ่งของรอบเวลาการนําเข้าเดียวกัน เอนทิตีอื่นๆ ต้องนําหน้าการสร้างรายการการเดินทาง มิฉะนั้น ค่าจะตรวจสอบความถูกต้องไม่ได้ หากมีการใช้ค่าตัวยึดสำหรับหมายเลขการเดินทางหรือใบแจ้งรายการ การเชื่อมโยงสามารถสร้างได้ก็ต่อเมื่อใช้ตัวยึดตัวเดียวกันกับสำหรับหมายเลขการเดินทางหรือใบแจ้งรายการในเอนทิตีรายการการเดินทาง

หากใบสั่งซื้อหรือรายการใบสั่งโอนย้ายได้รับการมอบหมายให้กับรายการการเดินทางที่มีอยู่แล้ว รายการการเดินทางใหม่จะไม่ถูกสร้างขึ้น ก่อนที่สามารถมอบหมายบรรทัดใบสั่งให้กับการเดินทางใหม่ได้ ต้องลบบรรทัดใบสั่งนั้นออกจากการเดินทางปัจจุบัน

### <a name="order-line-identification"></a>รหัสรายการใบสั่ง

บรรทัดการเดินทางอ้างอิงรหัสเรกคอร์ดอ้างอิงค่า **รหัสเรกคอร์ด** (`RefRecId`), **รหัสมิติสินค้าคงคลัง** (`InventDimId`) และ **รหัสธุรกรรมสินค้าคงคลัง** (`InventTransId`) โดยตรง ค่าเหล่านี้ไม่จำเป็นต้องรวมอยู่อีกต่อไปเมื่อมีการใช้เอนทิตีข้อมูล ขณะนี้ต้องรวมหมายเลขบรรทัดใบสั่งแทน เมื่อรวมกันแล้ว หมายเลขบรรทัดใบสั่งและหมายเลขใบสั่งจะช่วยให้สามารถระบุค่าอ้างอิงแต่ละค่าเหล่านั้นได้

### <a name="voyage-line-quantity"></a>ปริมาณรายการการเดินทาง

เนื่องจากรายการการเดินทางเชื่อมโยงกับรายการใบสั่งโดยตรง ค่า **ปริมาณ** (`ShipQty`) ที่ป้อนโดยใช้เอนทิตีต้องการให้ค่าตรงกัน การตรวจสอบความถูกต้องจะรันโดยเทียบกับปริมาณในบรรทัดใบสั่งซื้อหรือบรรทัดโอนย้าย หากการตรวจสอบความถูกต้องล้มเหลว เรกคอร์ดจะไม่มีการประมวลผล

### <a name="calculated-fields"></a>ฟิลด์ที่คำนวณได้

ฟิลด์ที่คำนวณได้ **น้ำหนัก** และ **ปริมาตร** ยอมรับค่าที่ได้รับผ่านเอนทิตีข้อมูล ถ้าไม่มีการระบุค่า ระบบจะใช้ค่าเพื่ออัปเดตฟิลด์เหล่านี้ ถ้าค่าของระบบพร้อมใช้งาน สำหรับต้นทุนแฝง ค่าจะถูกคํานวณในลักษณะต่อไปนี้

- *น้ำหนัก* = *ปริมาณ* × *น้ำหนักรวมของสินค้า*
- *ปริมาตร* = *ปริมาณ* × (*ความลึกรวมของสินค้า* × *ความสูงรวมของสินค้า* × *ความกว้างรวมของสินค้า*)

## <a name="sequencing"></a>การจัดลำดับ

เนื่องจากความเชื่อมโยงกันระหว่างตารางนี้ คุณต้องสร้างเรกคอร์ดการเดินทางก่อน บรรทัดการเดินทางสามารถสร้างขึ้นได้เฉพาะหลังจากการเดินทาง คอนเทนเนอร์ขนส่ง และใบแจ้งรายการได้ถูกสร้างขึ้นแล้วเท่านั้น

เมื่อต้องการสร้างการเดินทางโดยไม่มีคําเตือนการตรวจสอบความถูกต้อง ระบบต้องประมวลผลเอนทิตีตามลำดับดังนี้

1. การเดินทาง (`ITMTableEntity`)
1. คอนเทนเนอร์การจัดส่ง (`ITMContainersEntity`)
1. ใบแจ้งรายการ (`ITMFolioTableEntity`)
1. รายการการเดินทาง (`ITMPurchaseLinesEntity` หรือ `ITMTransferLinesEntity`)
