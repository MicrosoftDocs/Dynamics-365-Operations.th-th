---
title: การตั้งค่าสถานการณ์จำลองสำหรับเครื่องมือ IoT
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกสถานการณ์จำลองใน Supply Chain Management สำหรับเครื่องมือ IoT
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b87a9b73f49e73fe13b98fb11da939c9b30e0f6e
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386566"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="8350b-103">การตั้งค่าสถานการณ์จำลองสำหรับเครื่องมือ IoT</span><span class="sxs-lookup"><span data-stu-id="8350b-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8350b-104">หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกสถานการณ์จำลองใน Supply Chain Management สำหรับเครื่องมือ IoT</span><span class="sxs-lookup"><span data-stu-id="8350b-104">This topic describes how to configure a scenario in Supply Chain Management for IoT Intelligence.</span></span> <span data-ttu-id="8350b-105">ก่อนที่คุณจะสามารถตั้งค่าสถานการณ์จำลองได้ คุณต้อง [ตั้งค่า LCS](iot-lcs-setup.md)</span><span class="sxs-lookup"><span data-stu-id="8350b-105">Before you can setup the scenarios, you must [setup LCS](iot-lcs-setup.md).</span></span>

<span data-ttu-id="8350b-106">ในหัวข้อนี้คุณจะตั้งค่าคอนฟิกสถานการณ์จำลอง **การหยุดทำงานของอุปกรณ์** เพื่อสร้างการแจ้งเตือนใน Supply Chain Management เมื่อเครื่องจักรหยุดทำงาน</span><span class="sxs-lookup"><span data-stu-id="8350b-106">In this topic, you will configure the **Equipment downtime** scenario to generate a notification in Supply Chain Management when a machine goes down.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="8350b-107">ตั้งค่าคอนฟิกสถานการณ์จำลอง **การหยุดทำงานของอุปกรณ์** ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8350b-107">Configure the **Equipment downtime** scenario in Supply Chain Management</span></span>

<span data-ttu-id="8350b-108">สถานการณ์จำลอง **การหยุดทำงานของอุปกรณ์** แม็ปสัญญาณ Part Out ไปยังขีดจำกัดการแจ้งเตือนเครื่องจักร</span><span class="sxs-lookup"><span data-stu-id="8350b-108">The **Equipment downtime** scenario maps a part out signal to a machine alert threshold.</span></span> <span data-ttu-id="8350b-109">เครื่องจักรจะถูกตรวจสอบเฉพาะเมื่อมีการเลือกเครื่องจักรสำหรับสถานการณ์จำลองและตั้งค่าให้รันใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8350b-109">The machine is monitored only when the machine is selected for the scenario and is set to running in Supply Chain Management.</span></span> <span data-ttu-id="8350b-110">ถ้าเวลาตั้งแต่สัญญาณ Part Out ที่รับล่าสุดของเครื่องจักรที่ได้รับล่าสุดมากกว่าขีดจำกัด การแจ้งเตือน **เครื่องจักรหยุดทำงาน** จะถูกทริกเกอร์</span><span class="sxs-lookup"><span data-stu-id="8350b-110">If the time since the machine’s last received Part Out signal is greater than the alert threshold, then a **Machine down** notification is triggered.</span></span> <span data-ttu-id="8350b-111">ถ้าเครื่องจักรยังคงทำงานอยู่เมื่อได้รับสัญญาณ **PartOut** ถัดไป จะมีการทริกเกอร์การแจ้งเตือน **เครื่องจักรทำงาน**</span><span class="sxs-lookup"><span data-stu-id="8350b-111">If the machine is still running, when the next **PartOut** signal is received a **Machine up** notification is triggered.</span></span> <span data-ttu-id="8350b-112">ถ้าเครื่องจักรหยุดทำงานนาน 30 นาที การแจ้งเตือน **เครื่องจักรหยุดทำงาน** จะถูกทริกเกอร์</span><span class="sxs-lookup"><span data-stu-id="8350b-112">If a machine stays down for 30 mins a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="8350b-113">สถานการณ์จำลองของ **การหยุดทำงานของอุปกรณ์** มีความเชื่อมโยงต่อกันเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="8350b-113">The **Equipment downtime** scenario has these dependencies:</span></span>

+ <span data-ttu-id="8350b-114">ใบสั่งผลิตต้องรันบนเครื่องจักรที่ถูกแม็ปเพื่อให้การแจ้งเตือนถูกทริกเกอร์</span><span class="sxs-lookup"><span data-stu-id="8350b-114">A production order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="8350b-115">จะต้องส่งสัญญาณที่แสดงถึงสัญญาณ Part Out ของเครื่องจักรที่ถูกแม็ปไปยังฮับ IoT ที่มีชื่อคุณสมบัติที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="8350b-115">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="8350b-116">ต้องแสดงคุณสมบัติการลงเวลาของ Unix เป็นมิลลิวินาทีในข้อความฮับ IoT</span><span class="sxs-lookup"><span data-stu-id="8350b-116">A Unix milliseconds timestamp property must be present in the IoT hub message.</span></span>

<span data-ttu-id="8350b-117">ทำตามขั้นตอนเหล่านี้เพื่อตั้งค่าคอนฟิกสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="8350b-117">To configure the scenario, follow these steps:</span></span>

1. <span data-ttu-id="8350b-118">ลงชื่อเข้าใช้ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8350b-118">Log into Supply Chain Management.</span></span>
2. <span data-ttu-id="8350b-119">เปิดใช้งานข้อมูลแฟล็กลักษณะการทำงานของเครื่องมือ IoT</span><span class="sxs-lookup"><span data-stu-id="8350b-119">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="8350b-120">สำหรับข้อมูลเพิ่มเติม ดูที่ [ภาพรวมการจัดการคุณลักษณะ](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="8350b-120">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
3. <span data-ttu-id="8350b-121">ตั้งค่าคอนฟิกหน่วยเมตริก</span><span class="sxs-lookup"><span data-stu-id="8350b-121">Configure the metrics.</span></span> <span data-ttu-id="8350b-122">สำหรับข้อมูลเพิ่มเติมเกี่ยว ดูที่ [วิธีการตั้งค่าคอนฟิกหน่วยเมตริก](iot-metrics-setup.md#configure-metrics)</span><span class="sxs-lookup"><span data-stu-id="8350b-122">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="8350b-123">นำทางไปยังการ **ตัวควบคุมการผลิต**</span><span class="sxs-lookup"><span data-stu-id="8350b-123">Navigate to **Production control**.</span></span>
5. <span data-ttu-id="8350b-124">นำทางไปยังการ **ตั้งค่า \> เครื่องมือ IoT \> การจัดการสถานการณ์จำลอง**</span><span class="sxs-lookup"><span data-stu-id="8350b-124">Navigate to **Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="8350b-125">คลิก **ตั้งค่าคอนฟิก** บนไทล์ **การหยุดทำงานของอุปกรณ์**</span><span class="sxs-lookup"><span data-stu-id="8350b-125">Click **Configure** on the **Equipment downtime** tile.</span></span> <span data-ttu-id="8350b-126">วิซาร์ดการตั้งค่าคอนฟิกเริ่มต้นด้วยหน้า **นิยามเค้าร่างของเซ็นเซอร์อุปกรณ์**</span><span class="sxs-lookup"><span data-stu-id="8350b-126">The configuration wizard starts with the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="8350b-127">เป้าหมายที่นี่คือการตั้งค่าเค้าร่างใน Supply Chain Management ให้ตรงกับรูปแบบ JSON ของข้อความ IoT</span><span class="sxs-lookup"><span data-stu-id="8350b-127">The goal here is to setup the schema in Supply Chain Management to match the JSON format of the IoT messages.</span></span> <span data-ttu-id="8350b-128">สามารถกำหนดเค้าร่างข้อความหลายแบบได้</span><span class="sxs-lookup"><span data-stu-id="8350b-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="8350b-129">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [รูปแบบเค้าร่างข้อความสำหรับฮับ IoT](iot-schema-format.md)</span><span class="sxs-lookup"><span data-stu-id="8350b-129">For more information, see [Message schema formats for IoT Hub](iot-schema-format.md).</span></span> <span data-ttu-id="8350b-130">ในตัวอย่างนี้ ส่วนของข้อความนี้จะประกอบด้วยชุดของข้อความที่มีรูปแบบนี้ดังนี้</span><span class="sxs-lookup"><span data-stu-id="8350b-130">In this example, the message payload contains a batch of messages with this format:</span></span>

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. <span data-ttu-id="8350b-131">เพิ่มแถวลงในตาราง</span><span class="sxs-lookup"><span data-stu-id="8350b-131">Add a row to the table.</span></span>

    1. <span data-ttu-id="8350b-132">ตั้งค่า **ชื่อเค้าร่าง** เป็น **รหัส**</span><span class="sxs-lookup"><span data-stu-id="8350b-132">Set the **Schema name** to **ID**.</span></span>
    2. <span data-ttu-id="8350b-133">ตั้งค่า **พาธเค้าร่าง** เป็น **/payload[\*]/id**</span><span class="sxs-lookup"><span data-stu-id="8350b-133">Set the **Schema path** to **/payload[\*]/id**.</span></span>
    3. <span data-ttu-id="8350b-134">ตั้งค่า **คำอธิบาย** เป็น **รหัสข้อความ**</span><span class="sxs-lookup"><span data-stu-id="8350b-134">Set the **Description** to **Message ID**.</span></span>

8. <span data-ttu-id="8350b-135">เพิ่มแถวลงในตาราง</span><span class="sxs-lookup"><span data-stu-id="8350b-135">Add a row to the table.</span></span>

    1. <span data-ttu-id="8350b-136">ตั้งค่า **ชื่อเค้าร่าง** เป็น **การลงเวลา**</span><span class="sxs-lookup"><span data-stu-id="8350b-136">Set the **Schema name** to **Timestamp**.</span></span>
    2. <span data-ttu-id="8350b-137">ตั้งค่า **พาธเค้าร่าง** เป็น **/payload[\*]/timestamp**</span><span class="sxs-lookup"><span data-stu-id="8350b-137">Set the **Schema path** to **/payload[\*]/timestamp**.</span></span>
    3. <span data-ttu-id="8350b-138">ตั้งค่า **คำอธิบาย** เป็น **การลงเวลาข้อความ**</span><span class="sxs-lookup"><span data-stu-id="8350b-138">Set the **Description** to **Message timestamp**.</span></span>

9. <span data-ttu-id="8350b-139">เพิ่มแถวลงในตาราง</span><span class="sxs-lookup"><span data-stu-id="8350b-139">Add a row to the table.</span></span>

    1. <span data-ttu-id="8350b-140">ตั้งค่า **ชื่อเค้าร่าง** เป็น **ค่า**</span><span class="sxs-lookup"><span data-stu-id="8350b-140">Set the **Schema name** to **Value**.</span></span>
    2. <span data-ttu-id="8350b-141">ตั้งค่า **พาธเค้าร่าง** เป็น **/payload[\*]/value**</span><span class="sxs-lookup"><span data-stu-id="8350b-141">Set the **Schema path** to **/payload[\*]/value**.</span></span>
    3. <span data-ttu-id="8350b-142">ตั้งค่า **คำอธิบาย** เป็น **ค่าของข้อความ**</span><span class="sxs-lookup"><span data-stu-id="8350b-142">Set the **Description** to **Message value**.</span></span>

    <span data-ttu-id="8350b-143">คุณไม่จำเป็นต้องกำหนดคุณสมบัติทั้งหมดในข้อความ กำหนดเฉพาะที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="8350b-143">You don't need to define all the properties in the message, only the ones that you need.</span></span> <span data-ttu-id="8350b-144">ในตัวอย่างนี้ คุณไม่ได้สร้างแถวสำหรับการ **การลงเวลาของราก**</span><span class="sxs-lookup"><span data-stu-id="8350b-144">In this example, you did not create a row for **Root timestamp**.</span></span> <span data-ttu-id="8350b-145">พาธสำหรับการ **การลงเวลาของราก** จะเป็น **/timestamp**</span><span class="sxs-lookup"><span data-stu-id="8350b-145">The path for **Root timestamp** would be **/timestamp**.</span></span>
  
10. <span data-ttu-id="8350b-146">คลิก **ถัดไป** เพื่อไปยังหน้า **แม็ปเค้าร่างของเซ็นเซอร์อุปกรณ์**</span><span class="sxs-lookup"><span data-stu-id="8350b-146">Click **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="8350b-147">ในแถวสำหรับ **รหัสทรัพยากรอุปกรณ์** ตั้งค่า **ชื่อเค้าร่าง** เป็น **รหัส**</span><span class="sxs-lookup"><span data-stu-id="8350b-147">In the row for **Equipment resource ID** set the **Schema name** to **ID**.</span></span> <span data-ttu-id="8350b-148">ค่าที่ถูกต้องจะแสดงขึ้นในตารางแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="8350b-148">The valid values are displayed in a dropdown table.</span></span>
12. <span data-ttu-id="8350b-149">ในแถวสำหรับ **เวลา UTC** ให้ตั้งค่า **ชื่อเค้าร่าง** เป็น **การลงเวลา**</span><span class="sxs-lookup"><span data-stu-id="8350b-149">In the row for **UTC time** set the **Schema name** to **Timestamp**.</span></span> <span data-ttu-id="8350b-150">ค่าที่ถูกต้องจะแสดงขึ้นในตารางแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="8350b-150">The valid values are displayed in a dropdown table.</span></span>
13. <span data-ttu-id="8350b-151">ในแถวสำหรับ **สัญญาณที่ผลิตของส่วนประกอบ** ตั้งค่า **ชื่อเค้าร่าง** เป็น **ค่า**</span><span class="sxs-lookup"><span data-stu-id="8350b-151">In the row for **Part produced signal** set the **Schema name** to **Value**.</span></span> <span data-ttu-id="8350b-152">ค่าที่ถูกต้องจะแสดงขึ้นในตารางแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="8350b-152">The valid values are displayed in a dropdown table.</span></span>
14. <span data-ttu-id="8350b-153">คลิก **ถัดไป** สำหรับหน้า **การตั้งค่าคอนฟิกรหัสทรัพยากรอุปกรณ์**</span><span class="sxs-lookup"><span data-stu-id="8350b-153">Click **Next** for the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="8350b-154">ในขั้นตอนนี้คุณสามารถแม็ปค่าข้อความฮับ IoT กับทรัพยากร Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8350b-154">In this step, you map the IoT Hub message values to the Supply Chain Management resources.</span></span>

    1. <span data-ttu-id="8350b-155">ในตาราง **ค่าข้อมูลของสัญญาณ** ให้เพิ่มแถวใหม่และป้อน **IoTInt.Machine1225.PartOut** ในคอลัมน์ **ค่า**</span><span class="sxs-lookup"><span data-stu-id="8350b-155">In the **Signal Data Values** table, add a new row, and enter **IoTInt.Machine1225.PartOut** in the **Value** column.</span></span> <span data-ttu-id="8350b-156">ค่า **IoTInt.Machine1225.PartOut** มาจากคุณสมบัติ **รหัส** JSON ในข้อความฮับ IoT</span><span class="sxs-lookup"><span data-stu-id="8350b-156">The value **IoTInt.Machine1225.PartOut** comes from the JSON **id** property in the IoT hub message.</span></span>
    2. <span data-ttu-id="8350b-157">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8350b-157">Click **Save**.</span></span>
    3. <span data-ttu-id="8350b-158">ในตาราง **การแม็ปเรกคอร์ดธุรกิจ** ให้คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="8350b-158">In the **Business Record Mapping** table, click **New**.</span></span> <span data-ttu-id="8350b-159">ค่าเริ่มต้นสำหรับ **ชนิดเรกคอร์ดธุรกิจ** ถูกเติมโดยอัตโนมัติ และคุณไม่จำเป็นต้องเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="8350b-159">The default value for the **Business record type** is autopopulated, and you don't need to change it.</span></span>
    4. <span data-ttu-id="8350b-160">ในคอลัมน์ของ **เรกคอร์ดธุรกิจ** ให้เลือกทรัพยากรเครื่องจักร Supple Chain Management ที่ค่าสัญญาณนี้จะถูกส่งมา</span><span class="sxs-lookup"><span data-stu-id="8350b-160">In the **Business record** column, select the Supple Chain Management machine resource this signal value is being sent from.</span></span>
    5. <span data-ttu-id="8350b-161">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8350b-161">Click **Save**.</span></span>
    6. <span data-ttu-id="8350b-162">ทำซ้ำขั้นตอนเหล่านี้ เพิ่มการแม็ปเรกคอร์ดธุรกิจใหม่สำหรับ **Machine1226**</span><span class="sxs-lookup"><span data-stu-id="8350b-162">Repeat these steps, adding a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="8350b-163">คุณสามารถแม็ปค่าข้อมูลของสัญญาณหลายค่ากับเรกคอร์ดเดียวใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8350b-163">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="8350b-164">ใช้คอลัมน์ **ที่เลือก** เพื่อเลือกว่าคุณต้องการประมวลผลเครื่องจักรใด</span><span class="sxs-lookup"><span data-stu-id="8350b-164">Use the **Selected** column to choose which machines you want to process.</span></span> <span data-ttu-id="8350b-165">คุณไม่จำเป็นต้องกำหนดค่าสัญญาณทั้งหมดและคุณไม่จำเป็นต้องเลือกเครื่องจักรทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="8350b-165">You do not have to define all signal values and you do not have to select all machines.</span></span>
17. <span data-ttu-id="8350b-166">คลิก **ถัดไป** เพื่อไปที่หน้า **การตั้งค่าคอนฟิกของสัญญาณที่ผลิตของส่วนประกอบ**</span><span class="sxs-lookup"><span data-stu-id="8350b-166">Click **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="8350b-167">ในตาราง **ค่าข้อมูลของสัญญาณ** ให้เพิ่มแถวและตั้งค่า **ค่า** เป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="8350b-167">In the **Signal Data Values** table, add a row, and set **Value** to **True**.</span></span> <span data-ttu-id="8350b-168">ค่า **จริง** มาจากคุณสมบัติ **ค่า** JSON ในข้อความฮับ IoT</span><span class="sxs-lookup"><span data-stu-id="8350b-168">The value **True** comes from the JSON **value** property in the IoT hub message.</span></span> <span data-ttu-id="8350b-169">คุณสามารถเพิ่มค่ามากเท่าที่คุณต้องการสำหรับสถานการณ์จำลองของคุณ</span><span class="sxs-lookup"><span data-stu-id="8350b-169">You can add as many values as you need for your scenario.</span></span>
19. <span data-ttu-id="8350b-170">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8350b-170">Click **Save**.</span></span>
20. <span data-ttu-id="8350b-171">คลิก **ถัดไป** เพื่อไปยังหน้า **ขีดจำกัดการหยุดทำงานของอุปกรณ์**</span><span class="sxs-lookup"><span data-stu-id="8350b-171">Click **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="8350b-172">เครื่องจักรแสดงรายการเป็นเครื่องจักรที่ถูกแม็ปไปยังค่าสัญญาณก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="8350b-172">The machines listed are the machines previously mapped to signal values.</span></span> <span data-ttu-id="8350b-173">ในขั้นตอนนี้คุณจะกำหนดขีดจำกัดเพื่อตรวจสอบว่าเครื่องจักรหยุดทำงานหรือไม่</span><span class="sxs-lookup"><span data-stu-id="8350b-173">In this step, you define a threshold to determine if a machine is down.</span></span> <span data-ttu-id="8350b-174">ตัวอย่างเช่น ถ้าคุณตั้งค่าขีดจำกัดเป็น 10 Supply Chain Management จะสร้างข้อความแจ้งเตือนถ้าไม่มีข้อความ Part Out จากเครื่องจักรเป็นเวลา 10 นาที</span><span class="sxs-lookup"><span data-stu-id="8350b-174">For example, if you set the threshold to 10, Supply Chain Management generates a notification if there is no part out message from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="8350b-175">คลิก **ถัดไป** เพื่อไปยังหน้า **เปิดใช้งานสถานการณ์จำลอง**</span><span class="sxs-lookup"><span data-stu-id="8350b-175">Click **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="8350b-176">สลับแถบเลื่อนเพื่อเปิดใช้งานสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="8350b-176">Toggle the slider to enable the scenario.</span></span>
22. <span data-ttu-id="8350b-177">คลิก **Finish**</span><span class="sxs-lookup"><span data-stu-id="8350b-177">Click **Finish**.</span></span>

<span data-ttu-id="8350b-178">การตั้งค่าสถานการณ์จำลองเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="8350b-178">The scenario setup is complete.</span></span> <span data-ttu-id="8350b-179">เครื่องมือ IoT จะเริ่มการประมวลผลข้อความฮับ IoT โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="8350b-179">IoT Intelligence will automatically start processing the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="8350b-180">ตั้งค่าคอนฟิกสถานการณ์จำลอง **คุณภาพผลิตภัณฑ์** ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8350b-180">Configure the **Product quality** scenario in Supply Chain Management</span></span>

<span data-ttu-id="8350b-181">สถานการณ์จำลอง **คุณภาพผลิตภัณฑ์** สร้างการแจ้งเตือนถ้าแอททริบิวต์ของสินค้าอยู่นอกช่วงที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="8350b-181">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="8350b-182">ตัวอย่างเช่น เซ็นเซอร์อาจส่งน้ำหนักของสินค้าแต่ละรายการไปยังฮับ IoT</span><span class="sxs-lookup"><span data-stu-id="8350b-182">For example, a sensor could send the weight of each item to IoT Hub.</span></span> <span data-ttu-id="8350b-183">ใน Supply Chain Management จะมีการสร้างการแจ้งเตือนถ้าสินค้ามีน้ำหนักเกินหรือเบาเกินไป</span><span class="sxs-lookup"><span data-stu-id="8350b-183">In Supply Chain Management, a notification would be generated if the item was too heavy or too light.</span></span>

<span data-ttu-id="8350b-184">สถานการณ์จำลองมีการเชื่อมโยงกันเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="8350b-184">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="8350b-185">ใบสั่งผลิตต้องรันบนเครื่องจักรที่ถูกแม็ปและผลิตผลิตภัณฑ์ที่มีแอททริบิวต์ชุดงานที่ถูกแม็ปเพื่อให้การแจ้งเตือนถูกทริกเกอร์</span><span class="sxs-lookup"><span data-stu-id="8350b-185">A Production Order must be running on a mapped machine and producing a product with a mapped batch attribute for an alert to be triggered.</span></span>
+ <span data-ttu-id="8350b-186">จะต้องส่งสัญญาณที่แสดงถึงแอททริบิวต์ของชุดงาน ไปยังฮับ IoT ที่มีชื่อคุณสมบัติที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="8350b-186">A signal representing the batch attribute must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="8350b-187">ต้องแสดงคุณสมบัติการลงเวลาของ Unix เป็นมิลลิวินาทีในข้อความฮับ IoT</span><span class="sxs-lookup"><span data-stu-id="8350b-187">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="8350b-188">ตั้งค่าคอนฟิกสถานการณ์จำลอง **ความล่าช้าในการผลิต** ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8350b-188">Configure the **Production delays** scenario in Supply Chain Management</span></span>

<span data-ttu-id="8350b-189">สถานการณ์จำลอง **ความล่าช้าในการผลิต** จะสร้างการแจ้งเตือนถ้าปริมาณการผลิตอยู่ต่ำกว่าค่าขีดจำกัด</span><span class="sxs-lookup"><span data-stu-id="8350b-189">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="8350b-190">ในสถานการณ์สมมตินี้มีการส่งสัญญาณ **PartOut** ไปยังฮับ IoT สำหรับสินค้าแต่ละรายการที่ผลิต</span><span class="sxs-lookup"><span data-stu-id="8350b-190">In this scenario, a **PartOut** signal is sent to IoT Hub for each item produced.</span></span> <span data-ttu-id="8350b-191">ใน Supply Chain Management จะมีการคำนวณความล่าช้าของใบสั่งตามระยะเวลาที่จะมีการจัดกำหนดการใบสั่งผลิตเพื่อรันจำนวนสินค้าที่ควรจะมีการผลิต ระยะเวลาที่งานได้รับการรัน และจำนวนสัญญาณ **PartOut** ที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="8350b-191">In Supply Chain Management, the order delay is calculated based on how long the production order is scheduled to run, how many items should be produced, how long the job has been running, and how many **PartOut** signals are received.</span></span> <span data-ttu-id="8350b-192">การแจ้งเตือนความล่าช้าจะถูกสร้างขึ้นถ้าจำนวนของสัญญาณ **PartOut** สำหรับงานอยู่ต่ำกว่าค่าขีดจำกัดของค่าที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="8350b-192">A delay notification would be generated if the number of the **PartOut** signals for the job falls below the threshold value of the expected value.</span></span>

<span data-ttu-id="8350b-193">สถานการณ์จำลองมีการเชื่อมโยงกันเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="8350b-193">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="8350b-194">ใบสั่งผลิตต้องรันบนเครื่องจักรที่ถูกแม็ปเพื่อให้การแจ้งเตือนถูกทริกเกอร์</span><span class="sxs-lookup"><span data-stu-id="8350b-194">A Production Order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="8350b-195">จะต้องส่งสัญญาณที่แสดงถึงสัญญาณ Part Out ของเครื่องจักรที่ถูกแม็ปไปยังฮับ IoT ที่มีชื่อคุณสมบัติที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="8350b-195">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="8350b-196">ต้องแสดงคุณสมบัติการลงเวลาของ Unix เป็นมิลลิวินาทีในข้อความฮับ IoT</span><span class="sxs-lookup"><span data-stu-id="8350b-196">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="how-to-disable-a-scenario"></a><span data-ttu-id="8350b-197">วิธีการปิดใช้งานสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="8350b-197">How to disable a scenario</span></span>

<span data-ttu-id="8350b-198">หากต้องการปิดใช้งานสถานการณ์จำลอง ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="8350b-198">To disable a scenario, follow these steps:</span></span>

1. <span data-ttu-id="8350b-199">ใน Supply Chain Management ให้นำทางไปยัง **การควบคุมการผลิต \> การตั้งค่า \> เครื่องมือ IoT \> การจัดการสถานการณ์จำลอง**</span><span class="sxs-lookup"><span data-stu-id="8350b-199">In Supply Chain Management, navigate to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="8350b-200">คลิก **ตั้งค่าคอนฟิก** บนสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="8350b-200">Click **Configure** on the scenario.</span></span>
3. <span data-ttu-id="8350b-201">คลิก **ถัดไป** เพื่อเข้าถึงแท็บวิซาร์ดล่าสุด</span><span class="sxs-lookup"><span data-stu-id="8350b-201">Click **Next** to get to the last wizard tab.</span></span>
4. <span data-ttu-id="8350b-202">สลับแถบเลื่อนเพื่อปิดใช้งานสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="8350b-202">Toggle the slider to disable the scenario.</span></span>
