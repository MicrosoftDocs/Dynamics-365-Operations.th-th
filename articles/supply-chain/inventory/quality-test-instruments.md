---
title: เครื่องมือการทดสอบการจัดการคุณภาพ
description: หัวข้อนี้จะอธิบายวิธีการสร้างเครื่องมือทดสอบเพื่อให้สามารถใช้การทดสอบกับใบสั่งตรวจสอบคุณภาพใน Microsoft Dynamics 365 Supply Chain Management
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc09021f89a9064a3140a726fca74e3eceab13da
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956850"
---
# <a name="quality-management-test-instruments"></a><span data-ttu-id="f0756-103">เครื่องมือการทดสอบการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0756-103">Quality management test instruments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0756-104">หัวข้อนี้จะอธิบายวิธีการสร้างเครื่องมือทดสอบเพื่อให้สามารถใช้การทดสอบกับใบสั่งตรวจสอบคุณภาพใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="f0756-104">This topic describes how to create test instruments that can be used for tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="f0756-105">คุณใช้หน้า **เครื่องมือทดสอบ** เพื่อกําหนดและดูรายละเอียดเกี่ยวกับอุปกรณ์ที่ใช้ในการทดสอบบนใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0756-105">You use the **Test instruments** page to define and view details about the devices that are used to perform tests on quality orders.</span></span> <span data-ttu-id="f0756-106">เครื่องมือทดสอบสามารถระบุหรือไม่ก็ได้</span><span class="sxs-lookup"><span data-stu-id="f0756-106">Test instruments are optional.</span></span> <span data-ttu-id="f0756-107">แต่สามารถช่วยให้ผู้ปฏิบัติงานด้านคุณภาพทราบว่าอุปกรณ์หรือเครื่องมือใดที่ผู้ปฏิบัติงานควรใช้ทดสอบเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="f0756-107">However, they can help quality workers know which device or tool they should use to perform a specific test.</span></span>

## <a name="test-instrument-example"></a><span data-ttu-id="f0756-108">ตัวอย่างเครื่องมือทดสอบ</span><span class="sxs-lookup"><span data-stu-id="f0756-108">Test instrument example</span></span>

<span data-ttu-id="f0756-109">คุณกำลังทดสอบส่วนประกอบไฟฟ้าต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="f0756-109">You're performing various tests on electrical components.</span></span> <span data-ttu-id="f0756-110">การทดสอบบางอย่างใช้เฉพาะแรงดันลัพธ์ของส่วนประกอบ การทดสอบหนึ่งใช้เฉพาะกับอุณหภูมิของการทดสอบ และการทดสอบหนึ่งใช้สำหรับน้ําหนัก</span><span class="sxs-lookup"><span data-stu-id="f0756-110">Some tests are for the voltage output of the components, one test is for their temperature, and one test is for their weight.</span></span> <span data-ttu-id="f0756-111">เครื่องมือ อุปกรณ์ หรืออุปกรณ์ต่าง ๆ ใช้ในการทดสอบแต่ละครั้งแตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="f0756-111">Different tools, devices, or equipment is used to perform each test.</span></span> <span data-ttu-id="f0756-112">ตัวอย่างเช่น มิเตอร์แรงดันใช้ในการวัดแรงดัน เทอร์โมมิเตอร์ใช้วัดอุณหภูมิและสเกลใช้ในการวัดน้ําหนัก</span><span class="sxs-lookup"><span data-stu-id="f0756-112">For example, a voltage meter is used to measure voltage, a thermometer is used to measure temperature, and a scale is used to measure weight.</span></span> <span data-ttu-id="f0756-113">คุณสามารถตั้งค่าคอนฟิกอุปกรณ์แต่ละชิ้นเป็นเครื่องมือทดสอบและระบุหน่วยวัดที่ควรบันทึกผลการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="f0756-113">You can configure each of these devices as a test instrument and indicate the unit of measure that the test results should be recorded in.</span></span> <span data-ttu-id="f0756-114">ตัวอย่างเช่น ผลลัพธ์จากมิเตอร์แรงดันจะถูกบันทึกเป็นโวลต์ ผลลัพธ์จากเทอร์โมมิเตอร์จะถูกบันทึกในหน่วยองศาฟาเรนไฮต์ หรือองศาเซลเซียส และผลลัพธ์จากสเกลจะถูกบันทึกในหน่วยปอนด์หรือกิโลกรัม</span><span class="sxs-lookup"><span data-stu-id="f0756-114">For example, results from the voltage meter are recorded in volts, results from the thermometer are recorded in degrees Fahrenheit or degrees Celsius, and results from the scale are recorded in pounds or kilograms.</span></span>

## <a name="create-a-test-instrument"></a><span data-ttu-id="f0756-115">การสร้างเครื่องมือทดสอบ</span><span class="sxs-lookup"><span data-stu-id="f0756-115">Create a test instrument</span></span>

1. <span data-ttu-id="f0756-116">ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> การควบคุมคุณภาพ \> เครื่องมือการทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="f0756-116">Go to **Inventory management \> Setup \> Quality control \> Test instruments**.</span></span>
1. <span data-ttu-id="f0756-117">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="f0756-117">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="f0756-118">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="f0756-118">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="f0756-119">**เครื่องมือการทดสอบ** – ป้อนรหัสหรือชื่อเฉพาะสำหรับเครื่องมือการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="f0756-119">**Test instrument** – Enter a unique ID or name for the test instrument.</span></span>
    - <span data-ttu-id="f0756-120">**คำอธิบาย** – ป้อนคำอธิบายโดยละเอียดของเครื่องมือการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="f0756-120">**Description** – Enter a detailed description of the test instrument.</span></span>
    - <span data-ttu-id="f0756-121">**หน่วย** – เลือกหน่วยที่เครื่องมือวัดผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="f0756-121">**Unit** – Select the unit that the instrument measures results in.</span></span> <span data-ttu-id="f0756-122">ฟิลด์ **ความละเอียด** จะถูกตั้งค่าโดยอัตโนมัติตามหน่วยที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="f0756-122">The **Precision** field is automatically set, based on the unit that you select.</span></span>

1. <span data-ttu-id="f0756-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f0756-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0756-124">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f0756-124">Additional resources</span></span>

- [<span data-ttu-id="f0756-125">การทดสอบการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0756-125">Quality management test</span></span>](quality-tests.md)
- [<span data-ttu-id="f0756-126">กลุ่มการทดสอบการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0756-126">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
