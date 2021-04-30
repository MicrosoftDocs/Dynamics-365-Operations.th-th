---
title: ตรวจสอบและจัดการเครื่องมือ IoT
description: หัวข้อนี้จะอธิบายถึงวิธีการตรวจสอบและจัดการเครื่องมือ IoT
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 86e20b9e60e890833c0eb8573e92c0fbb27f8c9a
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908430"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="af539-103">ตรวจสอบและจัดการเครื่องมือ IoT</span><span class="sxs-lookup"><span data-stu-id="af539-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="af539-104">หัวข้อนี้จะอธิบายถึงวิธีการตรวจสอบและจัดการเครื่องมือ IoT</span><span class="sxs-lookup"><span data-stu-id="af539-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a> <span data-ttu-id="af539-105">ตรวจสอบสถานการณ์จำลองใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="af539-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="af539-106">คุณสามารถตรวจสอบการประมวลผลเครื่องมือ IoT จากสถานที่ต่างๆ ดังนี้:</span><span class="sxs-lookup"><span data-stu-id="af539-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="af539-107">**โมดูล \> การควบคุมการผลิต \> การสอบถามและรายงาน \> เครื่องมือ IoT \> การแจ้งเตือน** – ดูรายการของการแจ้งเตือนที่ยังไม่ได้แก้ไข</span><span class="sxs-lookup"><span data-stu-id="af539-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="af539-108">**โมดูล \> การควบคุมการผลิต \> การสอบถามและรายงาน \> เครื่องมือ IoT \> การแจ้งเตือนที่ปิด** – ดูรายการของการแจ้งเตือนที่ยังไม่ได้แก้ไขหรือถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="af539-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="af539-109">**โมดูล \> การควบคุมการผลิต \> การสอบถามและรายงาน \> เครื่องมือ IoT \> คีย์การวัด** – ดูคีย์การวัดสำหรับแผนภูมิชุดเวลา **สถานะของทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="af539-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="af539-110">**โมดูล \> การควบคุมการผลิต \> การดำเนินการผลิต \> สถานะของทรัพยากร** – ติดตามการวัดเฉพาะโดยใช้กล่องโต้ตอบ **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="af539-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="af539-111">ถ้าสถานการณ์จำลองตรวจพบข้อยกเว้น การแจ้งเตือนจะแสดงรายละเอียดข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="af539-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="af539-112">**พื้นที่ทำงาน \> การจัดการจัดการระบบการผลิต \> การแจ้งเตือน** – ดูรายการของการแจ้งเตือนที่ยังไม่ได้แก้ไข</span><span class="sxs-lookup"><span data-stu-id="af539-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="af539-113">ปรับเปลี่ยนสถานการณ์จำลองเครื่องมือ IoT ที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="af539-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="af539-114">เมื่อสถานการณ์จำลองกำลังรันอยู่คุณสามารถทำการเปลี่ยนแปลงดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="af539-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="af539-115">เพิ่มข้อกำหนดของเค้าร่างเซ็นเซอร์ใหม่</span><span class="sxs-lookup"><span data-stu-id="af539-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="af539-116">เลือกค่าข้อมูลของสัญญาณใหม่</span><span class="sxs-lookup"><span data-stu-id="af539-116">Select new signal data values.</span></span>
+ <span data-ttu-id="af539-117">ยกเลิกการเลือกค่าข้อมูลของสัญญาณที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="af539-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="af539-118">เพิ่มและแม็ปค่าข้อมูลของสัญญาณใหม่</span><span class="sxs-lookup"><span data-stu-id="af539-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="af539-119">อัปเดตค่าขีดจำกัด</span><span class="sxs-lookup"><span data-stu-id="af539-119">Update threshold values.</span></span>

<span data-ttu-id="af539-120">เมื่อสถานการณ์จำลองกำลังรันอยู่ ห้ามทำการเปลี่ยนแปลงดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="af539-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="af539-121">ลบหรือปรับเปลี่ยนข้อกำหนดเค้าร่างใดๆ ที่มีการใช้งานอยู่ในปัจจุบันโดยสถานการณ์จำลองที่เปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="af539-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="af539-122">เปลี่ยนเส้นทางเค้าร่างที่เลือกของสถานการณ์จำลองที่เปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="af539-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="af539-123">ตัวเลือกการจำลอง</span><span class="sxs-lookup"><span data-stu-id="af539-123">Simulation options</span></span>

<span data-ttu-id="af539-124">คุณสามารถจำลองสัญญาณเครื่องจักรโรงงานได้</span><span class="sxs-lookup"><span data-stu-id="af539-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="af539-125">สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="af539-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="af539-126">เชื่อมต่อ IoT DevKit AZ3166 กับฮับ Azure IoT</span><span class="sxs-lookup"><span data-stu-id="af539-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="af539-127">เชื่อมต่อกับโปรแกรมจำลอง Raspberry Pi ออนไลน์กับฮับ Azure IoT (Node.js)</span><span class="sxs-lookup"><span data-stu-id="af539-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="af539-128">ภาพรวมส่วนช่วยดำเนินการของโซลูชันการจำลองอุปกรณ์</span><span class="sxs-lookup"><span data-stu-id="af539-128">Device Simulation solution accelerator overview</span></span>](/azure/iot-accelerators/iot-accelerators-device-simulation-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]