---
title: การตั้งค่าสถานการณ์จำลองสำหรับเครื่องมือ IoT
description: หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าคอนฟิกสถานการณ์จำลองสำหรับเครื่องมือ IoT ใน Microsoft Dynamics 365 Supply Chain Management
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
ms.openlocfilehash: 36be4a85dbbd28839afd45b6ed167b4c8181ae72
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909512"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="305c6-103">การตั้งค่าสถานการณ์จำลองสำหรับเครื่องมือ IoT</span><span class="sxs-lookup"><span data-stu-id="305c6-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="305c6-104">หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าคอนฟิกสถานการณ์จำลองสำหรับเครื่องมือ IoT ใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="305c6-104">This topic explains how to configure scenarios for IoT Intelligence in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="305c6-105">ก่อนที่คุณจะสามารถตั้งค่าสถานการณ์ คุณต้อง [ตั้งค่า Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md)</span><span class="sxs-lookup"><span data-stu-id="305c6-105">Before you can set up the scenarios, you must [set up Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>

<span data-ttu-id="305c6-106">ในหัวข้อนี้คุณจะตั้งค่าคอนฟิกสถานการณ์จำลอง **การหยุดทำงานของอุปกรณ์** เพื่อให้สร้างการแจ้งเตือนใน Supply Chain Management เมื่อเครื่องจักรหยุดทำงาน</span><span class="sxs-lookup"><span data-stu-id="305c6-106">In this topic, you will configure the **Equipment downtime** scenario so that a notification is generated in Supply Chain Management when a machine goes down.</span></span> <span data-ttu-id="305c6-107">หัวข้อนี้จะแสดงวิธีการตั้งค่าคอนฟิกสถานการณ์ **คุณภาพของผลิตภัณฑ์** เพื่อให้มีการสร้างการแจ้งเตือนถ้าแอททริบิวต์ของรายการอยู่นอกช่วงที่ระบุและวิธีการตั้งค่าคอนฟิกสถานการณ์ **การล่าช้าในการผลิต** เพื่อให้มีการสร้างการแจ้งเตือนถ้าปริมาณการผลิตต่ำกว่าค่าขีดจำกัด</span><span class="sxs-lookup"><span data-stu-id="305c6-107">The topic also shows how to configure the **Product quality** scenario so that a notification is generated if an attribute of an item is outside a specified range, and how to configure the **Production delays** scenario so that a notification is generated if the production throughput falls below a threshold value.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="305c6-108">ตั้งค่าคอนฟิกสถานการณ์จำลอง การหยุดทำงานของอุปกรณ์ ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="305c6-108">Configure the Equipment downtime scenario in Supply Chain Management</span></span>

<span data-ttu-id="305c6-109">สถานการณ์ **การหยุดทำงานของอุปกรณ์** แม็ปสัญญาณ **PartOut** ไปยังขีดจำกัดการแจ้งเตือนเครื่องจักร</span><span class="sxs-lookup"><span data-stu-id="305c6-109">The **Equipment downtime** scenario maps a **PartOut** signal to a machine alert threshold.</span></span> <span data-ttu-id="305c6-110">เครื่องจักรจะถูกตรวจสอบเฉพาะเมื่อมีการเลือกเครื่องจักรสำหรับสถานการณ์และเมื่อตั้งค่าเป็น **กำลังทำงาน** ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="305c6-110">The machine is monitored only when it's selected for the scenario and when is set to **Running** in Supply Chain Management.</span></span> <span data-ttu-id="305c6-111">ถ้าเวลาตั้งแต่สัญญาณ **PartOut** ที่รับล่าสุดของเครื่องจักรที่ได้รับล่าสุดมากกว่าขีดจำกัด การแจ้งเตือน **เครื่องจักรหยุดทำงาน** จะถูกทริกเกอร์</span><span class="sxs-lookup"><span data-stu-id="305c6-111">If the time since a **PartOut** signal was last received from the machine exceeds the alert threshold, a **Machine down** notification is triggered.</span></span> <span data-ttu-id="305c6-112">ถ้าเครื่องจักรยังคงทำงานอยู่จะมีการทริกเกอร์การแจ้งเตือน **เครื่องจักรทำงาน** เมื่อได้รับสัญญาณ **PartOut** ถัดไป</span><span class="sxs-lookup"><span data-stu-id="305c6-112">If the machine is still running, a **Machine up** notification is triggered when the next **PartOut** signal is received.</span></span> <span data-ttu-id="305c6-113">ถ้าเครื่องจักรหยุดทำงานนาน 30 นาที การแจ้งเตือน **เครื่องจักรหยุดทำงาน** จะถูกทริกเกอร์</span><span class="sxs-lookup"><span data-stu-id="305c6-113">If a machine stays down for 30 minutes, a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="305c6-114">สถานการณ์จำลองของ **การหยุดทำงานของอุปกรณ์** มีความเชื่อมโยงต่อกันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="305c6-114">The **Equipment downtime** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="305c6-115">การแจ้งเตือนถูกทริกเกอร์เฉพาะเมื่อใบสั่งผลิตทำงานอยู่บนเครื่องจักรที่ถูกแม็ป</span><span class="sxs-lookup"><span data-stu-id="305c6-115">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="305c6-116">จะต้องส่งสัญญาณที่แสดงถึงสัญญาณ **PartOut** ของเครื่องจักรที่ถูกแม็ปไปยังฮับ IoT และมีชื่อคุณสมบัติที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="305c6-116">A signal that represents a mapped machine's **PartOut** signal must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="305c6-117">คุณสมบัติ **การประทับเวลา** UNIX โดยที่ค่าแสดงเป็นมิลลิวินาที (ms) ต้องมีอยู่ในข้อความฮับ IoT ของ Azure</span><span class="sxs-lookup"><span data-stu-id="305c6-117">A UNIX **timestamp** property, where the value is expressed in milliseconds (ms), must be present in the Azure IoT Hub message.</span></span>

<span data-ttu-id="305c6-118">การตั้งค่าคอนฟิกสถานการณ์ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="305c6-118">To configure the scenario, follow these steps.</span></span>

1. <span data-ttu-id="305c6-119">ลงชื่อเข้าใช้ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="305c6-119">Sign in to Supply Chain Management.</span></span>
2. <span data-ttu-id="305c6-120">เปิดใช้งานข้อมูลแฟล็กลักษณะการทำงานของเครื่องมือ IoT</span><span class="sxs-lookup"><span data-stu-id="305c6-120">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="305c6-121">สำหรับข้อมูลเพิ่มเติม ดูที่ [ภาพรวมการจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="305c6-121">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
3. <span data-ttu-id="305c6-122">ตั้งค่าคอนฟิกหน่วยเมตริก</span><span class="sxs-lookup"><span data-stu-id="305c6-122">Configure the metrics.</span></span> <span data-ttu-id="305c6-123">สำหรับข้อมูลเพิ่มเติมเกี่ยว ดูที่ [วิธีการตั้งค่าคอนฟิกหน่วยเมตริก](iot-metrics-setup.md#configure-metrics)</span><span class="sxs-lookup"><span data-stu-id="305c6-123">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="305c6-124">ไปที่ **การควบคุมการผลิต \> การตั้งค่า \> เครื่องมือ IoT \> การจัดการสถานการณ์**</span><span class="sxs-lookup"><span data-stu-id="305c6-124">Go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="305c6-125">บนไทล์ **การหยุดทำงานของอุปกรณ์** ให้เลือก **ตั้งค่าคอนฟิก** เพื่อเปิดวิซาร์ดการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="305c6-125">On the **Equipment downtime** tile, select **Configure** to open the configuration wizard.</span></span>

   <span data-ttu-id="305c6-126">หน้าแรกในวิซาร์ดคือหน้า **นิยามเค้าร่างของเซ็นเซอร์อุปกรณ์**</span><span class="sxs-lookup"><span data-stu-id="305c6-126">The first page in the wizard is the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="305c6-127">ในหน้านี้ เป้าหมายของคุณคือการตั้งค่าเค้าร่างใน Supply Chain Management เพื่อให้ตรงกับรูปแบบ JavaScript Object Notation (JSON) ของข้อความฮับ IoT</span><span class="sxs-lookup"><span data-stu-id="305c6-127">On this page, your goal is to set up the schema in Supply Chain Management so that it matches the JavaScript Object Notation (JSON) format of the IoT Hub messages.</span></span> <span data-ttu-id="305c6-128">สามารถกำหนดเค้าร่างข้อความหลายแบบได้</span><span class="sxs-lookup"><span data-stu-id="305c6-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="305c6-129">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [รูปแบบเค้าร่างข้อความสำหรับฮับ IoT](iot-schema-format.md)</span><span class="sxs-lookup"><span data-stu-id="305c6-129">For more information, see [Schema formats for IoT Hub messages](iot-schema-format.md).</span></span> <span data-ttu-id="305c6-130">ในตัวอย่างนี้ ส่วนของข้อความนี้จะประกอบด้วยชุดของข้อความที่มีรูปแบบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="305c6-130">In this example, the message payload contains a batch of messages that has the following format.</span></span>

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

7. <span data-ttu-id="305c6-131">เพิ่มแถวลงในตาราง และตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="305c6-131">Add a row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="305c6-132">ตั้งค่าฟิลด์ **ชื่อเค้าร่าง** เป็น **รหัส**</span><span class="sxs-lookup"><span data-stu-id="305c6-132">Set the **Schema name** field to **ID**.</span></span>
    2. <span data-ttu-id="305c6-133">ตั้งค่าฟิลด์ **พาธเค้าร่าง** เป็น **/payload\[\*\]/id**</span><span class="sxs-lookup"><span data-stu-id="305c6-133">Set the **Schema path** field to **/payload\[\*\]/id**.</span></span>
    3. <span data-ttu-id="305c6-134">ตั้งค่าฟิลด์ **คำอธิบาย** เป็น **รหัสข้อความ**</span><span class="sxs-lookup"><span data-stu-id="305c6-134">Set the **Description** field to **Message ID**.</span></span>

8. <span data-ttu-id="305c6-135">เพิ่มอีกแถวลงในตาราง และตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="305c6-135">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="305c6-136">ตั้งค่าฟิลด์ **ชื่อเค้าร่าง** เป็น **การประทับเวลา**</span><span class="sxs-lookup"><span data-stu-id="305c6-136">Set the **Schema name** field to **Timestamp**.</span></span>
    2. <span data-ttu-id="305c6-137">ตั้งค่าฟิลด์ **พาธเค้าร่าง** เป็น **/payload\[\*\]/timestamp**</span><span class="sxs-lookup"><span data-stu-id="305c6-137">Set the **Schema path** field to **/payload\[\*\]/timestamp**.</span></span>
    3. <span data-ttu-id="305c6-138">ตั้งค่าฟิลด์ **คำอธิบาย** เป็น **การประทับเวลาข้อความ**</span><span class="sxs-lookup"><span data-stu-id="305c6-138">Set the **Description** field to **Message timestamp**.</span></span>

9. <span data-ttu-id="305c6-139">เพิ่มอีกแถวลงในตาราง และตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="305c6-139">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="305c6-140">ตั้งค่าฟิลด์ **ชื่อเค้าร่าง** เป็น **ค่า**</span><span class="sxs-lookup"><span data-stu-id="305c6-140">Set the **Schema name** field to **Value**.</span></span>
    2. <span data-ttu-id="305c6-141">ตั้งค่าฟิลด์ **พาธเค้าร่าง** เป็น **/payload\[\*\]/value**</span><span class="sxs-lookup"><span data-stu-id="305c6-141">Set the **Schema path** field to **/payload\[\*\]/value**.</span></span>
    3. <span data-ttu-id="305c6-142">ตั้งค่าฟิลด์ **คำอธิบาย** เป็น **ค่าข้อความ**</span><span class="sxs-lookup"><span data-stu-id="305c6-142">Set the **Description** field to **Message value**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="305c6-143">คุณไม่จำเป็นต้องกำหนดคุณสมบัติทั้งหมดในข้อความ</span><span class="sxs-lookup"><span data-stu-id="305c6-143">You don't have to define all the properties in the message.</span></span> <span data-ttu-id="305c6-144">กำหนดเฉพาะคุณสมบัติที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="305c6-144">Define only the properties that you require.</span></span> <span data-ttu-id="305c6-145">ในขั้นตอนก่อนหน้านี้ คุณไม่ได้สร้างแถวสำหรับ **การประทับเวลาระดับราก**</span><span class="sxs-lookup"><span data-stu-id="305c6-145">In the preceding steps, you didn't create a row for **Root timestamp**.</span></span> <span data-ttu-id="305c6-146">พาธสำหรับ **การประทับเวลาระดับราก** จะเป็น **/timestamp**</span><span class="sxs-lookup"><span data-stu-id="305c6-146">The path of **Root timestamp** would be **/timestamp**.</span></span>

10. <span data-ttu-id="305c6-147">เลือก **ถัดไป** เพื่อไปยังหน้า **แม็ปเค้าร่างของเซ็นเซอร์อุปกรณ์**</span><span class="sxs-lookup"><span data-stu-id="305c6-147">Select **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="305c6-148">ในแถวสำหรับ **รหัสทรัพยากรอุปกรณ์** ในฟิลด์ **ชื่อเค้าร่าง** เลือก **รหัส**</span><span class="sxs-lookup"><span data-stu-id="305c6-148">In the row for **Equipment resource ID**, in the **Schema name** field, select **ID**.</span></span>
12. <span data-ttu-id="305c6-149">ในแถวสำหรับ **เวลา UTC** ในฟิลด์ **ชื่อเค้าร่าง** เลือก **การประทับเวลา**</span><span class="sxs-lookup"><span data-stu-id="305c6-149">In the row for **UTC time**, in the **Schema name** field, select **Timestamp**.</span></span>
13. <span data-ttu-id="305c6-150">ในแถวสำหรับ **สัญญาณที่ผลิตของส่วนประกอบ** ในฟิลด์ **ชื่อเค้าร่าง** เลือก **ค่า**</span><span class="sxs-lookup"><span data-stu-id="305c6-150">In the row for **Part produced signal**, in the **Schema name** field, select **Value**.</span></span>
14. <span data-ttu-id="305c6-151">เลือก **ถัดไป** เพื่อไปที่หน้า **การตั้งค่าคอนฟิกรหัสทรัพยากรอุปกรณ์**</span><span class="sxs-lookup"><span data-stu-id="305c6-151">Select **Next** to go to the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="305c6-152">ทำตามขั้นตอนเหล่านี้เพื่อแม็ปค่าในข้อความฮับ IoT กับทรัพยากร Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="305c6-152">Follow these steps to map the values in the IoT Hub message to the Supply Chain Management resources:</span></span>

    1. <span data-ttu-id="305c6-153">ในตาราง **ค่าข้อมูลของสัญญาณ** ให้เพิ่มแถวใหม่</span><span class="sxs-lookup"><span data-stu-id="305c6-153">In the **Signal Data Values** table, add a new row.</span></span> <span data-ttu-id="305c6-154">ในฟิลด์ **ค่า** ให้ป้อน **IoTInt.Machine1225.PartOut**</span><span class="sxs-lookup"><span data-stu-id="305c6-154">In the **Value** field, enter **IoTInt.Machine1225.PartOut**.</span></span> <span data-ttu-id="305c6-155">ค่านี้มาจากคุณสมบัติ **รหัส** JSON ในข้อความฮับ IoT</span><span class="sxs-lookup"><span data-stu-id="305c6-155">This value  comes from the JSON **id** property in the IoT Hub message.</span></span>
    2. <span data-ttu-id="305c6-156">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="305c6-156">Select **Save**.</span></span>
    3. <span data-ttu-id="305c6-157">ในตาราง **การแม็ปเรกคอร์ดธุรกิจ** ให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="305c6-157">In the **Business Record Mapping** table, select **New**.</span></span> <span data-ttu-id="305c6-158">ค่าเริ่มต้นสำหรับฟิลด์ **ชนิดเรกคอร์ดธุรกิจ** ถูกเติมโดยอัตโนมัติ และคุณไม่จำเป็นต้องเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="305c6-158">A default value for the **Business record type** field is automatically filled in, and you don't have to change it.</span></span>
    4. <span data-ttu-id="305c6-159">ในฟิลด์ **เรกคอร์ดธุรกิจ** ให้เลือกทรัพยากรเครื่องจักร Supply Chain Management ที่ค่าสัญญาณนี้จะถูกส่งมา</span><span class="sxs-lookup"><span data-stu-id="305c6-159">In the **Business record** field, select the Supply Chain Management machine resource that the signal value is being sent from.</span></span>
    5. <span data-ttu-id="305c6-160">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="305c6-160">Select **Save**.</span></span>
    6. <span data-ttu-id="305c6-161">ทำซ้ำขั้นตอนเหล่านี้เพื่อเพิ่มการแม็ปเรกคอร์ดธุรกิจใหม่สำหรับ **Machine1226**</span><span class="sxs-lookup"><span data-stu-id="305c6-161">Repeat these steps to add a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="305c6-162">คุณสามารถแม็ปค่าข้อมูลของสัญญาณหลายค่ากับเรกคอร์ดเดียวใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="305c6-162">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="305c6-163">ใช้คอลัมน์ **ที่เลือก** เพื่อเลือกเครื่องจักรที่คุณต้องการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="305c6-163">Use the **Selected** column to select the machines that you want to process.</span></span> <span data-ttu-id="305c6-164">คุณไม่จำเป็นต้องกำหนดค่าสัญญาณทั้งหมดและคุณไม่จำเป็นต้องเลือกเครื่องจักรทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="305c6-164">You don't have to define all signal values, and you don't have to select all machines.</span></span>
17. <span data-ttu-id="305c6-165">เลือก **ถัดไป** เพื่อไปที่หน้า **การตั้งค่าคอนฟิกของสัญญาณที่ผลิตของส่วนประกอบ**</span><span class="sxs-lookup"><span data-stu-id="305c6-165">Select **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="305c6-166">ในตาราง **ค่าข้อมูลของสัญญาณ** ให้เพิ่มแถวและตั้งค่าฟิลด์ **ค่า** เป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="305c6-166">In the **Signal Data Values** table, add a row, and set the **Value** field to **True**.</span></span> <span data-ttu-id="305c6-167">ค่านี้มาจากคุณสมบัติ **ค่า** JSON ในข้อความฮับ IoT</span><span class="sxs-lookup"><span data-stu-id="305c6-167">This value comes from the JSON **value** property in the IoT Hub message.</span></span> <span data-ttu-id="305c6-168">คุณสามารถเพิ่มค่ามากเท่าที่คุณต้องการสำหรับสถานการณ์จำลองของคุณ</span><span class="sxs-lookup"><span data-stu-id="305c6-168">You can add as many values as you require for your scenario.</span></span>
19. <span data-ttu-id="305c6-169">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="305c6-169">Select **Save**.</span></span>
20. <span data-ttu-id="305c6-170">เลือก **ถัดไป** เพื่อไปยังหน้า **ขีดจำกัดการหยุดทำงานของอุปกรณ์**</span><span class="sxs-lookup"><span data-stu-id="305c6-170">Select **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="305c6-171">เครื่องจักรแสดงรายการเป็นเครื่องจักรที่ถูกแม็ปไปยังค่าสัญญาณก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="305c6-171">The machines that are listed are the machines that were previously mapped to signal values.</span></span> <span data-ttu-id="305c6-172">ในหน้านี้ คุณจะกำหนดขีดจำกัดเพื่อตรวจสอบว่าเครื่องจักรหยุดทำงานหรือไม่</span><span class="sxs-lookup"><span data-stu-id="305c6-172">On this page, you will define a threshold to determine whether a machine is down.</span></span> <span data-ttu-id="305c6-173">ตัวอย่างเช่น ถ้าคุณตั้งค่าขีดจำกัดเป็น **10** Supply Chain Management จะสร้างข้อความแจ้งเตือนถ้าไม่ได้รับสัญญาณ **PartOut** จากเครื่องจักรเป็นเวลา 10 นาที</span><span class="sxs-lookup"><span data-stu-id="305c6-173">For example, if you set the threshold to **10**, Supply Chain Management will generate a notification if no **PartOut** signal is received from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="305c6-174">เลือก **ถัดไป** เพื่อไปยังหน้า **เปิดใช้งานสถานการณ์จำลอง**</span><span class="sxs-lookup"><span data-stu-id="305c6-174">Select **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="305c6-175">ตั้งค่าตัวเลือกเพื่อเปิดใช้งานสถานการณ์</span><span class="sxs-lookup"><span data-stu-id="305c6-175">Set the option to enable the scenario.</span></span>
22. <span data-ttu-id="305c6-176">เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="305c6-176">Select **Finish**.</span></span>

<span data-ttu-id="305c6-177">การตั้งค่าสถานการณ์เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="305c6-177">The scenario setup is now completed.</span></span> <span data-ttu-id="305c6-178">เครื่องมือ IoT จะเริ่มการประมวลผลข้อความฮับ IoT โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="305c6-178">IoT Intelligence will automatically start to process the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="305c6-179">ตั้งค่าคอนฟิกสถานการณ์จำลอง คุณภาพผลิตภัณฑ์ ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="305c6-179">Configure the Product quality scenario in Supply Chain Management</span></span>

<span data-ttu-id="305c6-180">สถานการณ์จำลอง **คุณภาพผลิตภัณฑ์** สร้างการแจ้งเตือนถ้าแอททริบิวต์ของสินค้าอยู่นอกช่วงที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="305c6-180">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="305c6-181">ตัวอย่างเช่น เซ็นเซอร์ส่งน้ำหนักของสินค้าแต่ละรายการไปยังฮับ IoT</span><span class="sxs-lookup"><span data-stu-id="305c6-181">For example, a sensor sends the weight of each item to IoT Hub.</span></span> <span data-ttu-id="305c6-182">ถ้าสินค้ามีน้ำหนักเกินหรือเบาเกินไป จะมีการสร้างการแจ้งเตือนใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="305c6-182">If an item is too heavy or too light, a notification is generated in Supply Chain Management.</span></span>

<span data-ttu-id="305c6-183">สถานการณ์ **คุณภาพของผลิตภัณฑ์** มีความเชื่อมโยงต่อกันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="305c6-183">The **Product quality** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="305c6-184">การแจ้งเตือนสามารถทริกเกอร์เฉพาะเมื่อมีการเรียกใช้ใบสั่งผลิตภัณฑ์บนเครื่องจักรที่ถูกแม็ปและผลิตผลิตภัณฑ์ที่มีแอททริบิวต์ชุดงานที่ถูกแม็ป</span><span class="sxs-lookup"><span data-stu-id="305c6-184">An alert can be triggered only if a production order is running on a mapped machine and producing a product that has a mapped batch attribute.</span></span>
+ <span data-ttu-id="305c6-185">จะต้องส่งสัญญาณที่แสดงถึงแอททริบิวต์ของชุดงานไปยังฮับ IoT และมีชื่อคุณสมบัติที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="305c6-185">A signal that represents the batch attribute must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="305c6-186">คุณสมบัติ **การประทับเวลา** UNIX โดยที่ค่าแสดงเป็น ms ต้องมีอยู่ในข้อความฮับ IoT</span><span class="sxs-lookup"><span data-stu-id="305c6-186">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="305c6-187">ตั้งค่าคอนฟิกสถานการณ์จำลอง ความล่าช้าในการผลิต ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="305c6-187">Configure the Production delays scenario in Supply Chain Management</span></span>

<span data-ttu-id="305c6-188">สถานการณ์จำลอง **ความล่าช้าในการผลิต** จะสร้างการแจ้งเตือนถ้าปริมาณการผลิตอยู่ต่ำกว่าค่าขีดจำกัด</span><span class="sxs-lookup"><span data-stu-id="305c6-188">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="305c6-189">ในสถานการณ์นี้ มีการส่งสัญญาณ **PartOut** ไปยังฮับ IoT สำหรับสินค้าแต่ละรายการที่ผลิต</span><span class="sxs-lookup"><span data-stu-id="305c6-189">In this scenario, a **PartOut** signal is sent to IoT Hub for each item that is produced.</span></span> <span data-ttu-id="305c6-190">ใน Supply Chain Management จะมีการคำนวณการล่าช้าของใบสั่งตามจำนวนเวลาที่ใบสั่งผลิตมีการจัดกำหนดการให้ทำงาน จำนวนของสินค้าที่ควรจะผลิต จำนวนของเวลาที่งานกำลังดำเนินอยู่ และจำนวนของสัญญาณ **PartOut** ที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="305c6-190">In Supply Chain Management, the order delay is calculated based on the amount of time that the production order is scheduled to run, the number of items that should be produced, the amount of time that the job has been running, and the number of **PartOut** signals that are received.</span></span> <span data-ttu-id="305c6-191">การแจ้งเตือนความล่าช้าถูกสร้างขึ้นถ้าจำนวนของสัญญาณ **PartOut** สำหรับงานอยู่ต่ำกว่าค่าขีดจำกัด</span><span class="sxs-lookup"><span data-stu-id="305c6-191">A delay notification is generated if the number of **PartOut** signals for the job falls below the threshold value.</span></span>

<span data-ttu-id="305c6-192">สถานการณ์ **การล่าช้าในการผลิต** มีความเชื่อมโยงต่อกันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="305c6-192">The **Production delays** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="305c6-193">การแจ้งเตือนถูกทริกเกอร์เฉพาะเมื่อใบสั่งผลิตทำงานอยู่บนเครื่องจักรที่ถูกแม็ป</span><span class="sxs-lookup"><span data-stu-id="305c6-193">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="305c6-194">จะต้องส่งสัญญาณที่แสดงถึงสัญญาณ **PartOut** ของเครื่องจักรที่ถูกแม็ปไปยังฮับ IoT ของ Azure และมีชื่อคุณสมบัติที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="305c6-194">A signal that represents a mapped machine's **PartOut** signal must be sent to the Azure IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="305c6-195">คุณสมบัติ **การประทับเวลา** UNIX โดยที่ค่าแสดงเป็น ms ต้องมีอยู่ในข้อความฮับ IoT</span><span class="sxs-lookup"><span data-stu-id="305c6-195">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="disable-a-scenario"></a><span data-ttu-id="305c6-196">ปิดใช้งานสถานการณ์</span><span class="sxs-lookup"><span data-stu-id="305c6-196">Disable a scenario</span></span>

<span data-ttu-id="305c6-197">หากต้องการปิดใช้งานสถานการณ์จำลอง ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="305c6-197">To disable a scenario, follow these steps.</span></span>

1. <span data-ttu-id="305c6-198">ใน Supply Chain Management ให้ไปยัง **การควบคุมการผลิต \> การตั้งค่า \> เครื่องมือ IoT \> การจัดการสถานการณ์**</span><span class="sxs-lookup"><span data-stu-id="305c6-198">In Supply Chain Management, go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="305c6-199">บนไทล์สำหรับสถานการณ์ ให้เลือก **ตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="305c6-199">On the tile for the scenario, select **Configure**.</span></span>
3. <span data-ttu-id="305c6-200">เลือก **ถัดไป** เพื่อไปยังหน้าสุดท้ายของวิซาร์ด</span><span class="sxs-lookup"><span data-stu-id="305c6-200">Select **Next** to go to the last wizard page.</span></span>
4. <span data-ttu-id="305c6-201">ตั้งค่าตัวเลือกเพื่อปิดใช้งานสถานการณ์</span><span class="sxs-lookup"><span data-stu-id="305c6-201">Set the option to disable the scenario.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]