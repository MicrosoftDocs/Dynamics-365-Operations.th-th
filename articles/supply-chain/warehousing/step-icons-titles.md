---
title: กําหนดไอคอนและชื่อขั้นตอนสำหรับแอป Warehouse Management บนมือถือ
description: บทความนี้อธิบายวิธีการกําหนดไอคอนและชื่อขั้นตอนให้กับโฟลว์งานใหม่หรือที่กําหนดเองสำหรับแอป Warehouse Management บนมือถือ
author: Mirzaab
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 361ace454f7125ec86bd99cffefc7d268f81d37f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890609"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a>กําหนดไอคอนและชื่อขั้นตอนสำหรับแอป Warehouse Management บนมือถือ

[!include [banner](../includes/banner.md)]

บทความนี้อธิบายวิธีการกําหนดไอคอนขั้นตอนและชื่อขั้นตอนให้กับโฟลว์งานใหม่หรือที่กําหนดเองสำหรับแอป Warehouse Management บนมือถือ

ภาพประกอบต่อไปนี้จะแสดงวิธีที่ไอคอนและชื่อขั้นตอนปรากฏในแอป Warehouse Management บนมือถือ

![ตัวอย่างของไอคอนขั้นตอนและชื่อขั้นตอนในแอปสำหรับอุปกรณ์เคลื่อนที่ Warehouse Management](media/step-icon-example.png "ตัวอย่างของไอคอนขั้นตอนและชื่อขั้นตอนในแอป Warehouse Management บนมือถือ")

## <a name="turn-this-feature-on-or-off"></a>เปิดหรือปิดคุณลักษณะนี้

หากต้องการใช้ฟังก์ชันที่อธิบายไว้ในบทความนี้ คุณต้องเปิดคุณลักษณะ *การตั้งค่าผู้ใช้ ไอคอน และชื่อขั้นตอนต่างๆ ของคุณลักษณะแอปคลังสินค้าใหม่* ในระบบของคุณ เริ่มจาก Supply Chain Management รุ่น 10.0.25 คุณลักษณะนี้เป็นแบบบังคับและไม่สามารถปิดได้ ถ้าคุณเรียกใช้รุ่นที่เก่ากว่า 10.0.25 ผู้ดูแลระบบสามารถเปิดหรือปิดฟังก์ชันนี้ได้โดยค้นหาคุณลักษณะ *การตั้งค่าผู้ใช้ ไอคอน และชื่อขั้นตอนต่างๆ ของคุณลักษณะแอปคลังสินค้าใหม่* ในพื้นที่ทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

## <a name="standard-step-ids-classes-and-icons"></a>รหัส คลาส และไอคอนขั้นตอนมาตรฐาน

แต่ละขั้นตอนในโฟลว์งานจะถูกระบุโดยรหัสขั้นตอน และแต่ละรหัสขั้นตอนมีคลาสขั้นตอนที่ตรงกัน ไอคอนขั้นตอนและชื่อจะระบุอยู่ในแต่ละคลาสขั้นตอน

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a>รหัสขั้นตอนและคลาสขั้นตอน

ตารางต่อไปนี้แสดงรายการรหัสขั้นตอนทุกรหัสที่พร้อมใช้งานในปัจจุบัน และคลาสขั้นตอนที่ตรงกัน ชื่อตัวควบคุมของฟิลด์ป้อนข้อมูลหลักถูกใช้เป็นรหัสขั้นตอน

สำหรับตัวอย่างที่แสดงว่ามีการใช้รหัสขั้นตอนและคลาสเหล่านี้อย่างไร โปรดดูที่การใช้งานของวิธีการ `WHSMobileAppStepInfoBuilder.stepId()` ใน [ตัวอย่าง: กําหนดไอคอนขั้นตอนและชื่อให้กับส่วนโฟลว์ที่กําหนดเอง](#example) ในภายหลังในบทความนี้

| รหัสขั้นตอน | คลาสขั้นตอน |
|-|-|
| BatchDisposition | WHSMobileAppStepBatchDisposition |
| ผู้ขนส่ง | WHSMobileAppStepCarrier |
| CatchWeight | WHSMobileAppStepCatchWeight |
| CatchWeightQtyOutboundWeight | WHSMobileAppStepCatchWeight |
| CatchWeightTag | WHSMobileAppStepCatchWeightTag |
| CatchWeightTagWeight | WHSMobileAppStepCatchWeightTagWeight |
| ChangeWarehouseSuccess | WHSMobileAppStepChangeWarehouseSuccess |
| CheckDigit | WHSMobileAppStepCheckDigit |
| ClusterId | WHSMobileAppStepClusterId |
| ClusterPickQtyVerification | WHSMobileAppStepQtyVerification |
| ClusterPosition | WHSMobileAppStepClusterPosition |
| ConfigId | WHSMobileAppStepConfigId |
| ใบสั่งขาย | WHSMobileAppStepConfirmation |
| ConsolidateFromLicensePlateId | WHSMobileAppStepConsolidateFromLicensePlateId |
| ConsolidateLPConfirmation | WHSMobileAppStepConsolidateLPConfirmation |
| ConsolidateToLicensePlateId | WHSMobileAppStepConsolidateToLicensePlateId |
| ContainerType | WHSMobileAppStepContainerType |
| CountingReasonCode | WHSMobileAppStepCountingReasonCode |
| CycleCountingAddLPOrFinish | WHSMobileAppStepCycleCountingAddLPOrFinish |
| CycleCountQty1 | WHSMobileAppStepCycleCountQty |
| CycleCountQty2 | WHSMobileAppStepCycleCountQty |
| CycleCountQty3 | WHSMobileAppStepCycleCountQty |
| CycleCountQty4 | WHSMobileAppStepCycleCountQty |
| Disposition | WHSMobileAppStepDisposition |
| DriverCheckInConfirmation | WHSMobileAppStepDriverCheckInConfirmation |
| DriverCheckInId | WHSMobileAppStepDriverCheckInId |
| DriverCheckOutConfirmation | WHSMobileAppStepDriverCheckOutConfirmation |
| DriverCheckOutId | WHSMobileAppStepDriverCheckOutId |
| ExpDate | WHSMobileAppStepExpDate |
| FromBatchDisposition | WHSMobileAppStepFromBatchDisposition |
| FromInventoryStatus | WHSMobileAppStepInventoryStatusFrom |
| FullQty | WHSMobileAppStepFullQty |
| InboundPut | WHSMobileAppStepInboundPut |
| InventBatchId | WHSMobileAppStepBatch |
| InventColorId | WHSMobileAppStepInventColorId |
| InventLocation | WHSMobileAppStepInventLocation |
| InventLocationId | WHSMobileAppStepWarehouse |
| InventSerialId | WHSMobileAppStepInventSerialId |
| InventSizeId | WHSMobileAppStepInventSizeId |
| InventStatusId | WHSMobileAppStepInventStatus |
| InventStyleId | WHSMobileAppStepInventStyleId |
| InventVersionId | WHSMobileAppStepInventVersionId |
| ItemId | WHSMobileAppStepItem |
| ITMContainerID | ITMMobileAppStepContainerId |
| ITMShipmentID | ITMMobileAppStepContainerId |
| KanbanCardId | WHSMobileAppStepKanbanCard |
| KanbanCardToEmpty | WHSMobileAppStepKanbanCardToEmpty |
| KanbanOrCardId | WHSMobileAppStepKanbanCard |
| LicensePlateId | WHSMobileAppStepLicensePlate |
| LoadId | WHSMobileAppStepLoadId |
| LocationLicensePlatePosition | WHSMobileAppStepLocationLicensePlatePosition |
| LocOrLP | WHSMobileAppStepLocOrLP |
| LocOrLP_From | WHSMobileAppStepLocOrLPFrom |
| LocOrLP_To | WHSMobileAppStepLocOrLPTo |
| LocOrLPCheck | WHSMobileAppStepLocOrLPCheck |
| LocVerification | WHSMobileAppStepLocVerification |
| LPAdjustIn | WHSMobileAppStepLPAdjustIn |
| LPBreakChildLP | WHSMobileAppStepLPBreakChildLP |
| LPBreakParentLP | WHSMobileAppStepLPBreakParentLP |
| LPBuildChildLP | WHSMobileAppStepLPBuildChildLP |
| LPBuildParentLP | WHSMobileAppStepLPBuildParentLP |
| LPVerification | WHSMobileAppStepLPVerification |
| MergeContainerId | WHSMobileAppStepMergeContainerId |
| MixedLPLineNum | WHSMobileAppStepMixedLPLineNum |
| MobileDeviceQueueMessageCollectionIdentifierId | WHSMobileAppStepSelectOrder |
| MovementConfirmCancel | WHSMobileAppStepMovementConfirmCancel |
| NewCaptureWeight | WHSMobileAppStepCatchWeight |
| NewQty | WHSMobileAppStepNewQty |
| OutboundCatchWeightTag | WHSMobileAppStepCatchWeightTag |
| OutboundPut | WHSMobileAppStepOutboundPut |
| OutboundWeight | WHSMobileAppStepCatchWeight |
| OverridePutNewLocation | WHSMobileAppStepOverridePutNewLocation |
| PieceByPieceConfirmation | WHSMobileAppStepQtyVerification |
| POLineNum | WHSMobileAppStepPOLineNum |
| หมายเลขใบสั่งซื้อ | WHSMobileAppStepPONum |
| PositionFull | WHSMobileAppStepPositionFull |
| PositionFullQty | WHSMobileAppStepPositionFullQty |
| ความแข็งแรง | WHSMobileAppStepPotency |
| PrinterName | WHSMobileAppStepPrinterName |
| ProdId | WHSMobileAppStepProdId |
| ProdLastPalletConfirmation | WHSMobileAppStepProdLastPalletConfirmation |
| ProductConfirmation | WHSMobileAppStepProductConfirmation |
| ProductionScrapConfirmation | WHSMobileAppStepProductionScrapConfirmation |
| ส่งสินค้า | WHSMobileAppStepPut |
| PutawayClusterId | WHSMobileAppStepPutawayClusterId |
| ปริมาณ | WHSMobileAppStepQty |
| QtyAdjust | WHSMobileAppStepQtyAdjust |
| QtyShort | WHSMobileAppStepQtyShort |
| QtyToConsume | WHSMobileAppStepQtyToConsume |
| QtyToPick | WHSMobileAppStepQtyToPick |
| QtyToPut | WHSMobileAppStepQtyToPut |
| QtyToScrap | WHSMobileAppStepQtyToScrap |
| QtyVerification | WHSMobileAppStepQtyVerification |
| QtyWithscanningLimit | WHSMobileAppStepQtyAdjust |
| ReasonString | WHSMobileAppStepReasonString |
| RecvLocationId | WHSMobileAppStepRecvLocationId |
| RemoveContainerId | WHSMobileAppStepRemoveContainerId |
| ReprintLabelConfirmation | WHSMobileAppStepReprintLabelConfirmation |
| RMANum | WHSMobileAppStepRMANum |
| ShortPickReason | WHSMobileAppStepShortPickReason |
| SortConOrLP | WHSMobileAppStepSortConOrLP |
| SortLicensePlateId | WHSMobileAppStepSortLicensePlateId |
| SortPositionId | WHSMobileAppStepSortPositionId |
| SortVerification | WHSMobileAppStepSortVerification |
| StartLocationId | WHSMobileAppStepStartLocationId |
| StartProdOrderConfirmation | WHSMobileAppStepStartProdOrderConfirmation |
| TargetLicensePlateId | WHSMobileAppStepTargetLicensePlateId |
| TOLineNum | WHSMobileAppStepTOLineNum |
| ToLocation | WHSMobileAppStepToLocation |
| TONum | WHSMobileAppStepTONum |
| ToWarehouse | WHSMobileAppStepWarehouseTo |
| TransportLoadId | WHSMobileAppStepTransportLoadId |
| WaveLabelId | WHSMobileAppStepWaveLabelId |
| WaveLblQty | WHSMobileAppStepWaveLblQty |
| น้ำหนัก | WHSMobileAppStepWeight |
| WeightToConsume | WHSMobileAppStepWeightToConsume |
| WHSAdjustmentType | WHSMobileAppStepWHSAdjustmentType |
| WHSReceivingException | WHSMobileAppStepWHSReceivingException |
| WHSWorkException | WHSMobileAppStepWHSWorkException |
| WHSWorkLicensePlateId | WHSMobileAppStepWorkLicensePlateId |
| WMSLocationId | WHSMobileAppStepLocation |
| WorkId | WHSMobileAppStepWorkId |
| WorkIdToCancel | WHSMobileAppStepWorkIdToCancel |
| WorkLPIdPutawayCluster | WHSMobileAppStepWorkLPIdPutawayCluster |
| WorkPoolId | WHSMobileAppStepWorkPoolId |
| ZoneId | WHSMobileAppStepZoneId |

### <a name="available-step-icons"></a><a name="step-icons"></a>ไอคอนขั้นตอนที่มีอยู่

ระบบมีคอลเลกชันไอคอนขั้นตอนมาตรฐานที่คุณสามารถใช้กับขั้นตอนที่กำหนดเองของคุณ ขณะนี้คุณไม่สามารถอัปโหลดไอคอนขั้นตอนที่กำหนดเองได้ ดังนั้นคุณจึงต้องเลือกหนึ่งในไอคอนขั้นตอนมาตรฐานเสมอ

ตารางต่อไปนี้จะแสดงไอคอนขั้นตอนมาตรฐานทุกไอคอนที่พร้อมใช้งานในปัจจุบันและชื่อขั้นตอน

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="เกี่ยวกับไอคอนขั้นตอน"><br>เกี่ยวกับ</td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="เพิ่มไอคอนป้ายทะเบียนหรือขั้นตอนสินค้า"><br>AddLpOrItem</td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="ไอคอนขั้นตอนการโอนการครอบครองชุดงาน"><br>BatchDisposition</td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="ไอคอนขั้นตอนของผู้ขนส่ง"><br>ผู้ขนส่ง</td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="ไอคอนขั้นตอนแท็กน้ำหนักจริง"><br>CatchWeightTag</td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="ไอคอนขั้นตอนน้ำหนักของแท็กน้ำหนักจริง"><br>CatchWeightTagWeight</td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="ไอคอนขั้นตอนตัวเลขการตรวจสอบ"><br>CheckDigit</td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="ไอคอนขั้นตอนรหัสเช็คอินหรือเช็คเอาท์"><br>CheckInOutId</td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="ไอคอนขั้นตอนป้ายทะเบียนรอง"><br>ChildLP</td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="ไอคอนขั้นตอนรหัสคลัสเตอร์"><br>ClusterId</td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="ไอคอนขั้นตอนตําแหน่งคลัสเตอร์"><br>ClusterPosition</td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="ไอคอนขั้นตอนรหัสการกำหนด"><br>ConfigId</td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="ไอคอนขั้นตอนของฟิลด์ที่กำหนดค่า"><br>ConfiguredField</td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="ไอคอนขั้นตอนที่กำหนดค่าหรือป้ายทะเบียน"><br>ConOrLP</td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="ไอคอนขั้นตอนการรวมจากรหัสป้ายทะเบียนรวม"><br>ConsolidateFromLicensePlateID</td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="ไอคอนขั้นตอนการรวมเป็นรหัสป้ายทะเบียนรวม"><br>ConsolidateToLicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="ไอคอนขั้นตอนชนิดคอนเทนเนอร์"><br>ContainerType</td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="ไอคอนขั้นตอนการตรวจนับ"><br>การตรวจนับ</td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="ไอคอนขั้นตอนรหัสเหตุผลการตรวจนับ"><br>CountingReasonCode</td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="ไอคอนขั้นตอนรหัสประเทศผู้ผลิต"><br>CountryOfOrigin</td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="ไอคอนขั้นตอนการโอนการครอบครอง"><br>Disposition</td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="ไอคอนขั้นตอนเสร็จสิ้น"><br>ทำแล้ว</td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="ไอคอนขั้นตอนการยืนยันการเช็คอินของพนักงานขนส่ง"><br>DriverCheckInConfirmation</td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="ไอคอนขั้นตอนรหัสการเช็คอินของพนักงานขนส่ง"><br>DriverCheckInId</td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="ไอคอนขั้นตอนรหัสการเช็คเอาท์ของพนักงานขนส่ง"><br>DriverCheckOutId</td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="ไอคอนขั้นตอนวันหมดอายุ"><br>ExpDate</td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="ไอคอนขั้นตอนของฟิลด์"><br>ฟิลด์</td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="ไอคอนขั้นตอนจากการโอนการครอบครองชุดงาน"><br>FromBatchDisposition</td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="ไอคอนขั้นตอนสถานะสินค้าคงคลังเริ่มต้น"><br>FromInventoryStatus</td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="ไอคอนขั้นตอนแอททริบิวต์รหัส"><br>IdAttribute</td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="ไอคอนขั้นตอนรหัสชุดงานสินค้าคงคลัง"><br>InventBatchID</td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="ไอคอนขั้นตอนรหัสสีสินค้าคงคลัง"><br>InventColorID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="ไอคอนขั้นตอนที่ตั้งสินค้าคงคลัง"><br>InventLocation</td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="ไอคอนขั้นตอนรหัสลำดับประจำสินค้าคงคลัง"><br>InventSerialID</td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="ไอคอนขั้นตอนรหัสขนาดสินค้าคงคลัง"><br>InventSizeID</td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="ไอคอนขั้นตอนรหัสสถานะสินค้าคงคลัง"><br>InventStatusID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="ไอคอนขั้นตอนรหัสลักษณะสินค้าคงคลัง"><br>InventStyleID</td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="ไอคอนขั้นตอนรหัสรุ่นสินค้าคงคลัง"><br>InventVersionID</td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="ไอคอนขั้นตอนรหัสสินค้า"><br>ItemID</td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="ไอคอนขั้นตอนรหัสคอนเทนเนอร์ ITM"><br>ITMContainerID</td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="ไอคอนขั้นตอนรหัสการจัดส่ง ITM"><br>ITMShipmentID</td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="ไอคอนขั้นตอนรหัสบัตรคัมบัง"><br>KanbanCardID</td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="ไอคอนขั้นตอนรหัสบัตรหรือคัมบัง"><br>KanbanOrCardID</td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="ไอคอนขั้นตอนรหัสของป้ายทะเบียน"><br>LicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="ไอคอนขั้นตอนรหัสสินค้า"><br>LoadId</td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="ไอคอนขั้นตอนการกำหนดตำแหน่งป้ายทะเบียนตามสถานที่"><br>LocationLicensePlatePosition</td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="ไอคอนขั้นตอนป้ายทะเบียนหรือที่ตั้ง"><br>LocOrLP</td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="ไอคอนขั้นตอนการตรวจสอบป้ายทะเบียนหรือที่ตั้ง"><br>LocOrLPCheck</td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="ป้ายทะเบียนหรือที่ตั้งจากไอคอนขั้นตอน"><br>LocOrLPFrom</td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="ป้ายทะเบียนหรือที่ตั้งเป็นไอคอนขั้นตอน"><br>LocOrLPTo</td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="ไอคอนขั้นตอนของกระบวนการที่เสร็จสมบูรณ์แบบยาว"><br>LongProcessCompleted</td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="ไอคอนขั้นตอน LP หลักของการแบ่ง LP"><br>LPBreakParentLP</td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="ไอคอนขั้นตอนรหัสคอนเทนเนอร์การรวม"><br>MergeContainerId</td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="ไอคอนขั้นตอนหมายเลขรายการป้ายทะเบียนแบบผสม"><br>MixedLPLineNum</td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="ไอคอนขั้นตอนน้ำหนักของสินค้าขาออก"><br>OutboundWeight</td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="ไอคอนขั้นตอนของเจ้าของ"><br>เจ้าของ</td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="ไอคอนขั้นตอนป้ายทะเบียนหลัก"><br>ParentLP</td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="โปรดยืนยันไอคอนขั้นตอน"><br>PleaseConfirm</td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="ไอคอนขั้นตอนหมายเลขรายการใบสั่งซื้อ"><br>POLineNum</td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="ไอคอนขั้นตอนหมายเลขใบสั่งซื้อ"><br>หมายเลขใบสั่งซื้อ</td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="ไอคอนขั้นตอนตำแหน่งแบบเต็ม"><br>PositionFull</td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="ไอคอนขั้นตอนความแข็งแรง"><br>ความแข็งแรง</td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="ไอคอนขั้นตอนชื่อเครื่องพิมพ์"><br>PrinterName</td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="ไอคอนขั้นตอนรหัส Prod"><br>ProdId</td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="ไอคอนขั้นตอนการยืนยันผลิตภัณฑ์"><br>ProductConfirmation</td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="ไอคอนขั้นตอนการส่งสินค้า"><br>ส่งสินค้า</td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="ไอคอนขั้นตอนรหัสคลัสเตอร์การสำรองสินค้า"><br>PutawayClusterId</td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="ไอคอนขั้นตอนของปริมาณ"><br>ปริมาณ</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="การปรับปรุงปริมาณในไอคอนขั้นตอน"><br>QtyAdjustIn</td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="ไอคอนขั้นตอนแบบสั้นของปริมาณ"><br>QtyShort</td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="ไอคอนขั้นตอนปริมาณที่จะใช้"><br>QtyToConsume</td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="ไอคอนขั้นตอนปริมาณที่จะส่ง"><br>QtyToPut</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="ไอคอนขั้นตอนปริมาณที่จะขัดเกลา"><br>QtyToScrap</td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="ไอคอนขั้นตอนการยืนยันปริมาณ"><br>QuantityConfirmation</td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="ไอคอนขั้นตอนของงานสิ้นสุดการรายงานเมื่อเสร็จสมบูรณ์"><br>RAFEndJob</td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="ไอคอนขั้นตอนรหัสสถานที่รับ"><br>RecvLocationID</td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="ไอคอนขั้นตอนรหัสคอนเทนเนอร์การนำออก"><br>RemoveContainerID</td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="ไอคอนขั้นตอนหมายเลข RMA"><br>RMANum</td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="ไอคอนขั้นตอนของใบสั่งที่เลือก"><br>SelectOrder</td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="ไอคอนขั้นตอนเหตุผลการเบิกสินค้าระยะสั้น"><br>ShortPickReason</td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="ไอคอนขั้นตอนรหัสตําแหน่งเรียงลำดับ"><br>SortPositionId</td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="ไอคอนขั้นตอนรหัสของป้ายทะเบียนเป้าหมาย"><br>TargetLicensePlateId</td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="ไอคอนขั้นตอนหมายเลขรายการสุดท้าย"><br>ToLineNum</td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="ไอคอนขั้นตอนที่ตั้งสุดท้าย"><br>ToLocation</td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="ไอคอนขั้นตอนหมายเลขสุดท้าย"><br>ToNum</td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="ไอคอนขั้นตอนคลังสินค้าสุดท้าย"><br>ToWarehouse</td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="ไอคอนขั้นตอนรหัสการบรรทุกเพื่อขนส่ง"><br>TransportLoadId</td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="ไอคอนขั้นตอนรหัสชุดงานผู้จัดจำหน่าย"><br>VendBatchId</td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="ไอคอนขั้นตอนรหัสป้ายชื่อเวฟ"><br>WaveLabelId</td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="ไอคอนขั้นตอนปริมาณป้ายชื่อเวฟ"><br>WaveLblQty</td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="ไอคอนขั้นตอนน้ำหนัก"><br>น้ำหนัก</td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="ไอคอนขั้นตอนน้ำหนักที่จะใช้"><br>WeightToConsume</td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="ไอคอนขั้นตอนชนิดการปรับปรุง WHS"><br>WHSAdjustmentType</td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="ไอคอนขั้นตอนข้อยกเว้นการรับ WHS"><br>WHSReceivingException</td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="ไอคอนขั้นตอนรหัสที่ตั้ง WMS"><br>WMSLocationID</td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="ไอคอนขั้นตอนรหัสงาน"><br>WorkId</td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="ไอคอนขั้นตอนรหัสงานที่จะยกเลิก"><br>WorkIdToCancel</td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="ไอคอนขั้นตอนรหัสของป้ายทะเบียนงาน"><br>WorkLicensePlateId</td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="ไอคอนขั้นตอนคลัสเตอร์ของการสำรองสินค้าของรหัสของป้ายทะเบียนงาน"><br>WorkLPIDPutawayCluster</td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="ไอคอนขั้นตอนรหัสกลุ่มงาน"><br>WorkPoolID</td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="ไอคอนขั้นตอนรหัสโซน"><br>ZoneID</td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a>ตัวอย่าง: กําหนดไอคอนขั้นตอนและชื่อให้กับโฟลว์ที่กําหนดเอง

ตัวอย่างนี้อธิบายวิธีการตั้งค่าไอคอนขั้นตอนและชื่อขั้นตอนของโฟลว์งานที่กำหนดเอง สถานการณ์ดังกล่าวสร้างขึ้นจากตัวอย่างของโฟลว์งานที่กำหนดเอง ซึ่งนําเสนอและสำรวจไปในรายละเอียดเพิ่มเติมในประกาศบล็อกต่อไปนี้: [การกำหนดค่า Warehousing Mobile App](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app) โฟลว์งานจะใช้ได้กับวิธีต่อไปนี้:

1. แอปจะแสดงหน้าที่ขอให้ผู้ปฏิบัติงานระบุรหัสคอนเทนเนอร์ (ตัวอย่างเช่น โดยการสแกนบาร์โค้ด)
1. หากรหัสคอนเทนเนอร์ถูกต้อง แอปจะเปิดขึ้นหน้าใหม่ที่เตือนผู้ปฏิบัติงานเกี่ยวกับน้ําหนัก (หากรหัสคอนเทนเนอร์ไม่ถูกต้อง ผู้ปฏิบัติงานจะถูกส่งกลับไปที่หน้าแรก)
1. เมื่อผู้ปฏิบัติงานป้อนน้ําหนักที่ถูกต้อง ระบบจะจัดเก็บน้ําหนักและส่งคืนผู้ปฏิบัติงานไปที่หน้าแรก

ในแผนภาพต่อไปนี้แสดงโฟลว์งานนี้

![แผนภาพของโฟลว์งาน](media/step-icons-example-task-flow.png "แผนภาพของโฟลว์งาน")

### <a name="create-a-step-class-for-the-container-input-page"></a>สร้างคลาสขั้นตอนเกี่ยวกับหน้าข้อมูลป้อนเข้าคอนเทนเนอร์

หน้าข้อมูลป้อนเข้าคอนเทนเนอร์ช่วยให้ผู้ปฏิบัติงานสแกนหรือป้อนรหัสคอนเทนเนอร์

![หน้าข้อมูลป้อนเข้าคอนเทนเนอร์](media/step-icons-example-container-input.png "หน้าข้อมูลป้อนเข้าคอนเทนเนอร์")

ในหน้าข้อมูลป้อนเข้าคอนเทนเนอร์ ชื่อตัวควบคุมของฟิลด์ป้อนข้อมูลคือ `ContainerId` เนื่องจากชื่อตัวควบคุมนี้ไม่อยู่ใน [รายการรหัสขั้นตอน](#step-ids-classes) คุณจึงไม่พบขั้นตอนที่มีอยู่ซึ่งอิงตามรหัสขั้นตอน ดังนั้น คุณต้องสร้างคลาสขั้นตอนที่แสดงถึงขั้นตอน นี่คือตัวอย่าง

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

รหัสของไอคอนขั้นตอนจัดเก็บอยู่ในสมาชิกคลาส `defaultStepIcon` และชื่อขั้นตอนจัดเก็บอยู่ในสมาชิกคลาส `defaultStepTitle`

เมื่อต้องการกําหนดไอคอนขั้นตอน ให้ตั้งค่า `defaultStepIcon` เป็นหนึ่งในรหัสไอคอนที่แสดงรายการในส่วน [ไอคอนขั้นตอนที่พร้อมใช้งาน](#step-icons) ก่อนหน้าในบทความนี้

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a>ใช้ไอคอนขั้นตอนและชื่อมาตรฐานหรือที่กำหนดเองสำหรับอินพุทน้ำหนัก

หน้าอินพุทน้ําหนักให้ผู้ปฏิบัติงานป้อนน้ําหนัก

![หน้าอินพุทน้ําหนัก](media/step-icons-example-weight-input.png "หน้าอินพุทน้ําหนัก")

ในหน้าอินพุทน้ําหนัก ชื่อตัวควบคุมของฟิลด์ป้อนเข้าคือ `Weight` ซึ่งอยู่ใน [รายการของรหัสขั้นตอน](#step-ids-classes) ดังนั้นถ้าไอคอนขั้นตอนและชื่อที่กําหนดไว้ในคลาส `WHSMobileAppStepWeight` เป็นที่ยอมรับให้คุณ คุณจะไม่ต้องเปลี่ยนสิ่งใดในขั้นตอนนี้

อย่างไรก็ตาม หากคุณต้องการใช้ไอคอนหรือชื่ออื่นของขั้นตอนนี้ คุณสามารถแทนที่วิธีการ `stepId()` หรือวิธีการ `stepInfo()` ในคลาสโปรแกรมสร้าง แต่ละโฟลว์งานจะมีโปรแกรมสร้างข้อมูลขั้นตอนของตนเอง

#### <a name="override-the-stepid-method"></a>การแทนที่วิธีการ stepId()

ตัวอย่างต่อไปนี้แสดงวิธีการหนึ่งที่คุณสามารถปรับเปลี่ยนคลาสของโปรแกรมสร้างด้วยการแทนที่วิธีการ `stepId()`

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

จากนั้นให้คุณสร้างคลาสขั้นตอนในขั้นตอน `NewWeight` รหัสควรคล้ายกับรหัสสำหรับตัวอย่าง `ContainerId` ที่แสดงไว้ก่อนหน้านี้ในบทความนี้

#### <a name="override-the-stepinfo-method"></a>การแทนที่วิธีการ stepInfo()

ตัวอย่างต่อไปนี้แสดงวิธีการหนึ่งที่คุณสามารถปรับเปลี่ยนคลาสของโปรแกรมสร้างด้วยการแทนที่วิธีการ `stepInfo()`

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

จากนั้นให้คุณสร้างออบเจ็กต์ `WHSMobileAppStepInfo` และตั้งไอคอนและ/หรือชื่อโดยตรง

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [ติดตั้งและเชื่อมต่อแอปการบริหารคลังสินค้าบนอุปกรณ์เคลื่อนที่](install-configure-warehouse-management-app.md)
- [การตั้งค่าผู้ใช้ของอุปกรณ์เคลื่อนที่](mobile-device-user-settings.md)
