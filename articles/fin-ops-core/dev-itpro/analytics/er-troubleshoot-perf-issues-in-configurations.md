---
title: การแก้ไขปัญหาประสิทธิภาพการทํางานในการตั้งค่าคอนฟิก ER
description: หัวข้อนี้อธิบายวิธีการค้นหาและแก้ไขปัญหาประสิทธิภาพการทํางานในการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d77c2aad904ba911ac19009d6a981ea4153aaa48
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216876"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a><span data-ttu-id="80193-103">การแก้ไขปัญหาประสิทธิภาพการทํางานในการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="80193-103">Troubleshooting performance issues in ER configurations</span></span>

<span data-ttu-id="80193-104">หัวข้อนี้อธิบายวิธีการค้นหาและแก้ไขปัญหาประสิทธิภาพการทํางานใน [การตั้งค่าคอนฟิก](general-electronic-reporting.md) [การรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting.md#Configuration) (ER)</span><span class="sxs-lookup"><span data-stu-id="80193-104">This topic explains how to find and solve performance issues in [Electronic reporting](general-electronic-reporting.md) (ER) [configurations](general-electronic-reporting.md#Configuration).</span></span>

<span data-ttu-id="80193-105">โดยทั่วไป การตรวจสอบประสิทธิภาพจะประกอบด้วยหลายขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="80193-105">Typically, performance investigation consists of several steps.</span></span>

1. <span data-ttu-id="80193-106">[รวบรวม](#collecting-data) ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="80193-106">[Collect](#collecting-data) data.</span></span>
2. <span data-ttu-id="80193-107">วิเคราะห์ข้อมูลที่รวบรวมไว้</span><span class="sxs-lookup"><span data-stu-id="80193-107">Analyze the collected data.</span></span>
3. <span data-ttu-id="80193-108">ขึ้นอยู่กับผลการวิเคราะห์ ใช้การกําหนดค่า ER เพื่อ [ทําการเปลี่ยนแปลง](#making-changes) หรือตัดสินใจที่จะรวบรวมข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="80193-108">Based on the results of the analysis, use ER configurations to [make changes](#making-changes), or decide to collect more data.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="80193-109">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="80193-109">Troubleshooting</span></span>

### <a name="analyze-execution-time"></a><span data-ttu-id="80193-110">วิเคราะห์เวลาดําเนินการ</span><span class="sxs-lookup"><span data-stu-id="80193-110">Analyze execution time</span></span>

<span data-ttu-id="80193-111">เวลาดําเนินการอาจขึ้นอยู่กับปัจจัยที่คาดเดาไม่ได้ เช่น งานอื่นๆ ที่กําลังทํางานในสภาพแวดล้อมเดียวกันและการแคชที่ใช้ข้อมูลเมื่อมีการเรียกเป็นครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="80193-111">Execution time can depend on unpredictable factors, such as other tasks that are running in the same environment and caching that uses data when it's called for the first time.</span></span> <span data-ttu-id="80193-112">ดังนั้น คุณควรทําซ้ําการดําเนินการและการวัดหลายครั้ง</span><span class="sxs-lookup"><span data-stu-id="80193-112">Therefore, you should repeat the execution and measurement several times.</span></span>

<span data-ttu-id="80193-113">บางครั้ง ปัญหาประสิทธิภาพการทํางานไม่ได้เกิดจากการตั้งค่าคอนฟิกรูปแบบ ER ที่ใช้สําหรับการรายงาน</span><span class="sxs-lookup"><span data-stu-id="80193-113">Sometimes, performance issues aren't caused by an ER format configuration that is used for reporting.</span></span> <span data-ttu-id="80193-114">รหัสเหล่านี้เกิดจากรหัส X++ ที่ใช้ในการเปิดการตั้งค่าคอนฟิกรูปแบบ ER นั้นแทน</span><span class="sxs-lookup"><span data-stu-id="80193-114">Instead, they are caused by the X++ code that is used to open that ER format configuration.</span></span>

1. <span data-ttu-id="80193-115">ใน [ศูนย์การดำเนินการ](#infolog-time) หรือ [บันทึกเหตุการณ์](#event-log-time) ให้ดูที่เวลาดําเนินการของรายงาน</span><span class="sxs-lookup"><span data-stu-id="80193-115">In either the [Action center](#infolog-time) or the [event log](#event-log-time), look at the execution time of the report.</span></span>
2. <span data-ttu-id="80193-116">เปรียบเทียบเวลาดําเนินการของรายงานกับเวลาการดําเนินการทั้งหมดในสถานการณ์</span><span class="sxs-lookup"><span data-stu-id="80193-116">Compare the execution time of the report with the total execution time in the scenario.</span></span>
3. <span data-ttu-id="80193-117">ถ้าเวลาดําเนินการของรายงานน้อยกว่าเวลาดําเนินการทั้งหมด ให้พิจารณาปริมาณข้อมูลที่รายงานประมวลผลดังนี้</span><span class="sxs-lookup"><span data-stu-id="80193-117">If the execution time of the report is much less than the total execution time, consider the amount of data that the report processes:</span></span>

    - <span data-ttu-id="80193-118">ถ้ารายงานประมวลผลข้อมูลจํานวนเล็กน้อย ปัญหาอาจเกี่ยวข้องกับเวลาการโหลดของการกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="80193-118">If the report processes a small amount of data, the issue might involve the loading time of the configuration.</span></span>
    - <span data-ttu-id="80193-119">ถ้ารายงานประมวลผลข้อมูลจํานวนมาก ปัญหาอาจเกี่ยวข้องกับการประมวลผล X++ ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="80193-119">If the report processes a large amount of data, the issue might involve preprocessing X++.</span></span> <span data-ttu-id="80193-120">ใช้ [ตัวแยกวิเคราะห์การติดตาม](#analyze-trace-parser-trace) เพื่อวิเคราะห์กรณีและปัญหานี้</span><span class="sxs-lookup"><span data-stu-id="80193-120">Use [Trace parser](#analyze-trace-parser-trace) to analyze this case.</span></span>

    <span data-ttu-id="80193-121">สําหรับกรณีอื่นๆ ให้ดูที่ส่วนถัดไป</span><span class="sxs-lookup"><span data-stu-id="80193-121">For other cases, see the next sections.</span></span>

4. <span data-ttu-id="80193-122">รันการทดสอบหลายรายการที่เกี่ยวข้องกับจํานวนข้อมูลที่แตกต่างกันเพื่อกําหนดว่าเวลาดําเนินการขึ้นอยู่กับปริมาณข้อมูลอย่างไร</span><span class="sxs-lookup"><span data-stu-id="80193-122">Run multiple tests that involve different amounts of data to determine how the execution time depends on the amount of data.</span></span>

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a><span data-ttu-id="80193-123">วิเคราะห์การติดตาม Trace parser</span><span class="sxs-lookup"><span data-stu-id="80193-123">Analyze Trace parser traces</span></span>

<span data-ttu-id="80193-124">จัดเตรียมตัวอย่างเล็กๆ หรือรวบรวมการติดตามหลายรายการในระหว่างส่วนสุ่มของการสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="80193-124">Prepare a small example, or collect several traces during random parts of the report generation.</span></span>

<span data-ttu-id="80193-125">จากนั้น ใน [Trace parser](#trace-parser) ให้ทําการวิเคราะห์จากล่างขึ้นบนมาตรฐานและตอบคําถามต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="80193-125">Then, in [Trace parser](#trace-parser), do a standard bottom-to-up analysis, and answer the following questions:</span></span>

- <span data-ttu-id="80193-126">วิธีการยอดนิยมในแง่ของปริมาณการใช้เวลาคืออะไร</span><span class="sxs-lookup"><span data-stu-id="80193-126">What are the top methods in terms of time consumption?</span></span>
- <span data-ttu-id="80193-127">ส่วนใดของเวลาโดยรวมที่วิธีการเหล่านั้นใช้</span><span class="sxs-lookup"><span data-stu-id="80193-127">What part of the overall time do those methods use?</span></span>

<span data-ttu-id="80193-128">ตอบคําถามเดียวกันสําหรับการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="80193-128">Answer the same questions for queries.</span></span>

<span data-ttu-id="80193-129">หากคุณเห็นว่าวิธีการนั้นนําหน้าด้วย "ER" ให้ไปยังส่วนถัดไป</span><span class="sxs-lookup"><span data-stu-id="80193-129">If you see that methods are prefixed with "ER," move on to the next section.</span></span>

<span data-ttu-id="80193-130">หากคุณเห็นว่าวิธีการหรือการสอบถามมีต้นกําเนิดมาจากชุดแอปพลิเคชัน ให้พิจารณาการเพิ่มประสิทธิภาพทั่วไป (ตัวอย่างเช่น สร้างดัชนี)</span><span class="sxs-lookup"><span data-stu-id="80193-130">If you see that methods or queries originated in the application suite, consider generic optimizations (for example, create indexes).</span></span>

<span data-ttu-id="80193-131">วิเคราะห์จํานวนการเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="80193-131">Analyze the number of calls.</span></span> <span data-ttu-id="80193-132">ถ้าจํานวนสูงกว่าที่คาดไว้อย่างมาก ให้พิจารณาการแคชโหนดที่สอดคล้องกันของการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="80193-132">If the number is significantly higher than expected, consider caching the corresponding nodes of the configuration.</span></span>

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a><span data-ttu-id="80193-133">วิเคราะห์การเรียกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="80193-133">Analyze database calls</span></span>

<span data-ttu-id="80193-134">จัดเตรียมตัวอย่างที่มีข้อมูลจํานวนเล็กน้อย เพื่อให้คุณสามารถรวบรวม [การติดตาม ER](#electronic-reporting-traces) ได้</span><span class="sxs-lookup"><span data-stu-id="80193-134">Prepare an example that has a small amount of data, so that you can collect an [ER trace](#electronic-reporting-traces).</span></span>

<span data-ttu-id="80193-135">จากนั้นเปิดการติดตามในตัวออกแบบการแม็ปแบบจําลอง ER และดูที่ด้านล่างของหน้า</span><span class="sxs-lookup"><span data-stu-id="80193-135">Then open the trace in the ER model mapping designer, and look at the bottom of the page.</span></span> <span data-ttu-id="80193-136">ตอบคําถามต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="80193-136">Answer the following questions:</span></span>

- <span data-ttu-id="80193-137">มีการทําซ้ําการสอบถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="80193-137">Is there any query duplication?</span></span> <span data-ttu-id="80193-138">ถ้ามี ให้พิจารณาการแก้ไขอย่างใดอย่างหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="80193-138">If there is, consider one of the following fixes:</span></span>

    - <span data-ttu-id="80193-139">[ใช้การแคช](#use-caching) ถ้าคุณคิดว่ามีการเรียกหลายครั้งภายในเรกคอร์ดหลักเรกคอร์ดเดียว</span><span class="sxs-lookup"><span data-stu-id="80193-139">[Use caching](#use-caching) if you think that there are several calls inside one parent record.</span></span>
    - <span data-ttu-id="80193-140">[ใช้ฟิลด์จากการคํานวณที่มีพารามิเตอร์เป็นแคช](#cached-parameterized) ถ้าคุณคิดว่ามีการเรียกร้องให้มีเรกคอร์ดเดียวกันภายในเรกคอร์ดที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="80193-140">[Use a cached, parameterized calculated field](#cached-parameterized) if you think that there are calls to the same record inside different records.</span></span>
    - <span data-ttu-id="80193-141">[ใช้แหล่งข้อมูล **JOIN**](#use-join-datasource) ถ้าคุณต้องอ่านเรกคอร์ดที่แตกต่างกันจํานวนมากจากฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="80193-141">[Use a **JOIN** data source](#use-join-datasource) if you have to read to a substantial number of different records from a database.</span></span>

- <span data-ttu-id="80193-142">จํานวนแบบสอบถามและเรกคอร์ดที่นํามาใช้สอดคล้องกับจํานวนข้อมูลโดยรวมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="80193-142">Does the number of queries and fetched records correspond to the overall amount of data?</span></span> <span data-ttu-id="80193-143">ตัวอย่างเช่น ถ้าเอกสารมี 10 บรรทัด สถิติแสดงให้เห็นว่ารายงานแยกบรรทัด 10 บรรทัดหรือ 1,000 บรรทัด</span><span class="sxs-lookup"><span data-stu-id="80193-143">For example, if a document has 10 lines, do the statistics show that the report extracts 10 lines or 1,000 lines?</span></span> <span data-ttu-id="80193-144">ถ้าคุณมีเรกคอร์ดที่นํามาใช้จํานวนมาก ให้พิจารณาการแก้ไขอย่างใดอย่างหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="80193-144">If you have a substantial number of fetched records, consider one of the following fixes:</span></span>

    - <span data-ttu-id="80193-145">[ใช้ฟังก์ชัน **FILTER** แทนฟังก์ชัน **WHERE**](#filter) เพื่อประมวลผลข้อมูลบนฝั่ง SQL Server</span><span class="sxs-lookup"><span data-stu-id="80193-145">[Use the **FILTER** function instead of the **WHERE** function](#filter) to process data on the SQL Server side.</span></span>
    - <span data-ttu-id="80193-146">ใช้การแคชเพื่อหลีกเลี่ยงการดึงข้อมูลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="80193-146">Use caching to avoid fetching the same data.</span></span>
    - <span data-ttu-id="80193-147">[ใช้ฟังก์ชันข้อมูลที่เก็บรวบรวม](#collected-data) เพื่อหลีกเลี่ยงการนําข้อมูลเดียวกันมาใช้เพื่อสรุป</span><span class="sxs-lookup"><span data-stu-id="80193-147">[Use collected data functions](#collected-data) to avoid fetching the same data for summarization.</span></span>

### <a name="analyze-perfview-traces"></a><span data-ttu-id="80193-148">วิเคราะห์การติดตาม PerfView</span><span class="sxs-lookup"><span data-stu-id="80193-148">Analyze PerfView traces</span></span>

<span data-ttu-id="80193-149">[PerfView](#perfview) เป็นเครื่องมือสําหรับนักพัฒนาที่มีประสบการณ์</span><span class="sxs-lookup"><span data-stu-id="80193-149">[PerfView](#perfview) is a tool for experienced developers.</span></span> <span data-ttu-id="80193-150">สําหรับข้อมูลเพิ่มเติมเกี่ยวกับขั้นตอนต่อไปนี้ ให้ดูที่ [พื้นฐานการสืบสวนเวลานาฬิกาแขวน](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics)</span><span class="sxs-lookup"><span data-stu-id="80193-150">For more detailed information about the following steps, see [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span></span>

1. <span data-ttu-id="80193-151">รวบรวมการติดตามโดยใช้เวลาเธรด</span><span class="sxs-lookup"><span data-stu-id="80193-151">Collect a trace by using thread time.</span></span>
2. <span data-ttu-id="80193-152">รวมเฉพาะสแต็คที่ใช้ **runUnattended** เพื่อกรองเฉพาะเธรดที่มีการดําเนินการกําหนดค่า</span><span class="sxs-lookup"><span data-stu-id="80193-152">Include only stacks that use **runUnattended**, to filter only the thread that has configuration execution.</span></span> <span data-ttu-id="80193-153">(เพิ่ม **runUnattended** ในกล่องป้อนข้อมูล **IncPats**)</span><span class="sxs-lookup"><span data-stu-id="80193-153">(Add **runUnattended** to the **IncPats** input box.)</span></span>
3. <span data-ttu-id="80193-154">เก็บ CPU เครือข่าย และเวลาที่ถูกบล็อกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="80193-154">Fold all CPU, network, and blocked time.</span></span>
4. <span data-ttu-id="80193-155">โหลด [ค่าที่ตั้งล่วงหน้าของ ER สําหรับ PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml)</span><span class="sxs-lookup"><span data-stu-id="80193-155">Load [ER presets for PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span></span>
5. <span data-ttu-id="80193-156">เลือก **ER** \> **การตั้งค่าที่กำหนดไว้ล่วงหน้าอื่นๆ**</span><span class="sxs-lookup"><span data-stu-id="80193-156">Select **ER** \> **Other preset**.</span></span>
6. <span data-ttu-id="80193-157">ดูชื่อ:</span><span class="sxs-lookup"><span data-stu-id="80193-157">Look at the names:</span></span>

    - <span data-ttu-id="80193-158">คุณอาจเห็นรหัสแพลตฟอร์มที่ใช้เวลามากที่สุด</span><span class="sxs-lookup"><span data-stu-id="80193-158">You will probably see the platform code that consumes the most time.</span></span>
    - <span data-ttu-id="80193-159">คุณสามารถแตะสองครั้ง (หรือคลิกสองครั้ง) และผ่าน **ผู้เรียกใช้**</span><span class="sxs-lookup"><span data-stu-id="80193-159">You can double-tap (or double-click) and go up through **callees**.</span></span>

        <span data-ttu-id="80193-160">ถ้าคุณพบคลาสที่มีคํานําหน้าว่า "ERExpression" และถ้าคลาสเหล่านั้นเป็นฟังก์ชันที่เกี่ยวข้องกับสูตร คุณสามารถเดาชื่อฟังก์ชันตามชื่อคลาส และคุณสามารถดูที่ ER repo เพื่อดูแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="80193-160">If you find classes that have the prefix "ERExpression," and if they are functions that are related to formulas, you can guess the function name based on the class name, and you can look at the ER repo to view the attributes.</span></span>

### <a name="fixes"></a><span data-ttu-id="80193-161">แก้ไข</span><span class="sxs-lookup"><span data-stu-id="80193-161">Fixes</span></span>

- <span data-ttu-id="80193-162">ถ้าคุณเห็นว่าเวลาส่วนใหญ่ของ CPU ถูกใช้โดยแบบสอบถาม ให้ลองลดจํานวนแบบสอบถาม:</span><span class="sxs-lookup"><span data-stu-id="80193-162">If you see that most of the CPU time is consumed by queries, try to reduce the number of queries:</span></span>

    - <span data-ttu-id="80193-163">[ตรวจทานการติดตาม ER](#analyze-database-calls) สําหรับการสอบถามที่ซ้ํากัน</span><span class="sxs-lookup"><span data-stu-id="80193-163">[Review the ER trace](#analyze-database-calls) for duplicated queries.</span></span>
    - <span data-ttu-id="80193-164">ดูจํานวนเรกคอร์ดที่นํามาใช้ และประเมินจํานวนข้อมูลที่ควรนํามาใช้ในทางทฤษฎี</span><span class="sxs-lookup"><span data-stu-id="80193-164">See how many records are fetched, and evaluate how much data should theoretically be fetched.</span></span>

- <span data-ttu-id="80193-165">หากคุณเห็นว่าเวลาส่วนใหญ่ของ CPU ถูกใช้โดยฟังก์ชันที่ใช้ ให้ลองค้นหาตําแหน่งในการกําหนดค่าที่ใช้ทรัพยากรมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="80193-165">If you see that most of the CPU time is consumed by the functions that are used, try to find the place in the configuration that consumes the most resources.</span></span>
- <span data-ttu-id="80193-166">ถ้าคุณเห็นว่าเวลาส่วนใหญ่ของ CPU จะถูกใช้โดยฟังก์ชันการรวบรวมข้อมูล ให้พิจารณาแทนที่ด้วย *จัดกลุ่ม SQL โดย* ที่ด้านการแม็ปแบบจําลอง</span><span class="sxs-lookup"><span data-stu-id="80193-166">If you see that most of the CPU time is consumed by data collection functions, consider replacing them with *SQL group by* on the model mapping side.</span></span>

### <a name="collecting-data"></a><a name="collecting-data"></a><span data-ttu-id="80193-167">การรวบรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="80193-167">Collecting data</span></span>

<span data-ttu-id="80193-168">มีหลายวิธีในการรวบรวมข้อมูลที่มีอยู่ โดยขึ้นอยู่กับสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="80193-168">Depending on your environment, there are several ways to collect available data:</span></span>

- <span data-ttu-id="80193-169">รับเวลาทํางานทั้งหมด:</span><span class="sxs-lookup"><span data-stu-id="80193-169">Get the total running time:</span></span>

    - <span data-ttu-id="80193-170">จากศูนย์การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="80193-170">From the Action center</span></span>
    - <span data-ttu-id="80193-171">จากบันทึกเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="80193-171">From the event log</span></span>

- <span data-ttu-id="80193-172">โปรไฟล์การดําเนินการ:</span><span class="sxs-lookup"><span data-stu-id="80193-172">Profile the execution:</span></span>

    - <span data-ttu-id="80193-173">โดยใช้เครื่องมือ ER</span><span class="sxs-lookup"><span data-stu-id="80193-173">By using ER tools</span></span>
    - <span data-ttu-id="80193-174">โดยใช้ตัวแยกวิเคราะห์การติดตาม</span><span class="sxs-lookup"><span data-stu-id="80193-174">By using Trace parser</span></span>
    - <span data-ttu-id="80193-175">โดยใช้ PerfView</span><span class="sxs-lookup"><span data-stu-id="80193-175">By using PerfView</span></span>

#### <a name="collecting-data-in-a-production-environment"></a><span data-ttu-id="80193-176">การรวบรวมข้อมูลในสภาพแวดล้อมการผลิต</span><span class="sxs-lookup"><span data-stu-id="80193-176">Collecting data in a production environment</span></span>

<span data-ttu-id="80193-177">บางครั้งปัญหาสามารถทําซ้ําได้เฉพาะในสภาพแวดล้อมการผลิตเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="80193-177">Sometimes, issues can be reproduced only in a production environment.</span></span> <span data-ttu-id="80193-178">ข้อมูลสามารถรวบรวมด้วยวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="80193-178">Data can be collected in the following ways:</span></span>

- <span data-ttu-id="80193-179">โดยใช้การติดตาม [Trace parser](../perf-test/trace-trace-tutorial.md)</span><span class="sxs-lookup"><span data-stu-id="80193-179">By using [Trace parser](../perf-test/trace-trace-tutorial.md) traces</span></span>
- <span data-ttu-id="80193-180">โดยใช้การติดตาม [การดําเนินการ ER](trace-execution-er-troubleshoot-perf.md)</span><span class="sxs-lookup"><span data-stu-id="80193-180">By using [ER execution](trace-execution-er-troubleshoot-perf.md) traces</span></span>
- <span data-ttu-id="80193-181">โดยใช้เวลาดําเนินการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="80193-181">By using the total execution time</span></span>

#### <a name="collecting-data-in-a-development-environment"></a><span data-ttu-id="80193-182">การรวบรวมข้อมูลในสภาพแวดล้อมการพัฒนา</span><span class="sxs-lookup"><span data-stu-id="80193-182">Collecting data in a development environment</span></span>

<span data-ttu-id="80193-183">นอกจากเครื่องมือที่สามารถใช้ในสภาพแวดล้อมการผลิตแล้ว ยังมีเครื่องมือหลายอย่างที่คุณสามารถใช้ในสภาพแวดล้อมการพัฒนา:</span><span class="sxs-lookup"><span data-stu-id="80193-183">In addition to the tools that can be used in a production environment, there are several tools that you can use in a development environment:</span></span>

- <span data-ttu-id="80193-184">บันทึกเหตุการณ์ (Microsoft-Dynamics-ElectronicReporting)</span><span class="sxs-lookup"><span data-stu-id="80193-184">Event log (Microsoft-Dynamics-ElectronicReporting).</span></span> <span data-ttu-id="80193-185">บันทึกนี้สามารถให้เวลาในการดําเนินการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="80193-185">This log can give you the total execution time.</span></span>
- <span data-ttu-id="80193-186">เครื่องมือ .NET ทั่วไป เช่น PerfView</span><span class="sxs-lookup"><span data-stu-id="80193-186">Common .NET tools, such as PerfView.</span></span>

<span data-ttu-id="80193-187">นอกจากนี้สภาพแวดล้อมการพัฒนาช่วยให้คุณมีความยืดหยุ่นมากขึ้นในการทดลอง</span><span class="sxs-lookup"><span data-stu-id="80193-187">Additionally, a development environment gives you more flexibility to experiment.</span></span> <span data-ttu-id="80193-188">ตัวอย่างเช่น คุณสามารถปิดบางส่วนของรายงานเพื่อดูว่าเวลาดําเนินการได้รับผลกระทบอย่างไร</span><span class="sxs-lookup"><span data-stu-id="80193-188">For example, you can turn off parts of reports to see how the execution time is affected.</span></span>

### <a name="tools"></a><a name="tools"></a><span data-ttu-id="80193-189">เครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="80193-189">Tools</span></span>

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a><span data-ttu-id="80193-190">เวลาดําเนินการในศูนย์การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="80193-190">Execution time in the Action center</span></span>

<span data-ttu-id="80193-191">ER สามารถแสดงเวลาดําเนินการของการตั้งค่าคอนฟิกในศูนย์การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="80193-191">ER can show the execution time of the configuration in the Action center.</span></span> <span data-ttu-id="80193-192">ตัวเลือกนี้ใช้ได้เฉพาะกับผู้ใช้ที่ระบุและบริษัทที่ระบุ และสําหรับเซสชันแบบโต้ตอบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="80193-192">This option works only for a specific user and a specific company, and only for interactive sessions.</span></span> <span data-ttu-id="80193-193">เมื่อต้องการทําให้คุณลักษณะนี้พร้อมใช้งาน ให้ทําตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="80193-193">To make this feature available, follow these steps.</span></span>

1. <span data-ttu-id="80193-194">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="80193-194">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="80193-195">ในหน้า **การตั้งค่าคอนฟิก** บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** ในกลุ่ม **การตั้งค่าล่วงหน้า** เลือก **พารามิเตอร์ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="80193-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="80193-196">ในกล่องโต้ตอบ **พารามิเตอร์ผู้ใช้** ตั้งค่าตัวเลือก **แสดงเวลาการสร้างไฟล์** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="80193-196">In the **User parameters** dialog box, set the **Show file generation time** option to **Yes**.</span></span>

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a><span data-ttu-id="80193-197">เวลาดําเนินการในบันทึกเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="80193-197">Execution time in the event log</span></span>

1. <span data-ttu-id="80193-198">เปิดตัวแสดงเหตุการณ์ Windows</span><span class="sxs-lookup"><span data-stu-id="80193-198">Open Windows Event Viewer.</span></span>
2. <span data-ttu-id="80193-199">ภายใต้ **บันทึกของโปรแกรมประยุกต์และบริการ** ให้เปิด **Microsoft-Dynamics-ElectronicReporting/Operational**</span><span class="sxs-lookup"><span data-stu-id="80193-199">Under **Applications and Services logs**, open **Microsoft-Dynamics-ElectronicReporting/Operational**.</span></span>
3. <span data-ttu-id="80193-200">ค้นหาเหตุการณ์ **FormatMapingRun** ที่ **EventID=2** เนื่องจากเหตุการณ์เหล่านี้มีข้อมูลเกี่ยวกับเวลาที่ผ่านไป</span><span class="sxs-lookup"><span data-stu-id="80193-200">Look for **FormatMapingRun** events where **EventID=2**, because these events contain the information about elapsed time.</span></span>

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a><span data-ttu-id="80193-201">การติดตาม Trace parser</span><span class="sxs-lookup"><span data-stu-id="80193-201">Trace parser traces</span></span> 

<span data-ttu-id="80193-202">เนื่องจาก ER ดําเนินการใน X++ คุณสามารถใช้เครื่องมือ X++ ทั่วไปเพื่อวิเคราะห์ประสิทธิภาพได้</span><span class="sxs-lookup"><span data-stu-id="80193-202">Because ER is implemented in X++, you can use common X++ tools to analyze performance.</span></span> <span data-ttu-id="80193-203">สําหรับข้อมูลเพิ่มเติม ให้ดูที่ [ติดตามโดยใช้ Trace parser](../perf-test/trace-trace-tutorial.md)</span><span class="sxs-lookup"><span data-stu-id="80193-203">For more information, see [Take traces by using Trace parser](../perf-test/trace-trace-tutorial.md).</span></span>

<span data-ttu-id="80193-204">มีข้อจํากัดบางประการสําหรับวิธีนี้</span><span class="sxs-lookup"><span data-stu-id="80193-204">There are a few limitations to this approach.</span></span> <span data-ttu-id="80193-205">เนื่องจากส่วนหนึ่งของ ER ถูกนํามาใช้ใน C# รายละเอียดทั้งหมดจะไม่สามารถใช้ได้</span><span class="sxs-lookup"><span data-stu-id="80193-205">Because part of ER is implemented in C#, not all the details will be available.</span></span> <span data-ttu-id="80193-206">อย่างไรก็ตาม คุณสามารถดูรายละเอียดการใช้ข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="80193-206">However, you can view the data usage details.</span></span> <span data-ttu-id="80193-207">นอกจากนี้ การรันรายงานแบบยาวอาจเกินขีดจํากัดการจัดเก็บการติดตาม</span><span class="sxs-lookup"><span data-stu-id="80193-207">Additionally, long report runs can exceed trace storage limitations.</span></span>

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a><span data-ttu-id="80193-208">การติดตาม ER</span><span class="sxs-lookup"><span data-stu-id="80193-208">ER traces</span></span>

<span data-ttu-id="80193-209">ER สามารถรวบรวมการติดตามของตัวเองและมีเครื่องมือการจัดรูปแบบการแสดงข้อมูลและการวิเคราะห์สําหรับการติดตามเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="80193-209">ER can collect its own traces, and it has visualization and analysis tools for those traces.</span></span> <span data-ttu-id="80193-210">สำหรับข้อมูลเพิ่มเติม ให้ดู [ติดตามการดำเนินการของรูปแบบ ER เพื่อแก้ไขปัญหาประสิทธิภาพ](trace-execution-er-troubleshoot-perf.md)</span><span class="sxs-lookup"><span data-stu-id="80193-210">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

#### <a name="perfview"></a><a name="perfview"></a><span data-ttu-id="80193-211">PerfView</span><span class="sxs-lookup"><span data-stu-id="80193-211">PerfView</span></span>

<span data-ttu-id="80193-212">เนื่องจากทั้ง X++ และ ER มีการใช้งานที่ด้านบนของแพลตฟอร์ม .NET คุณสามารถใช้เครื่องมือ .NET ทั่วไปได้</span><span class="sxs-lookup"><span data-stu-id="80193-212">Because both X++ and ER are implemented on top of the .NET platform, you can use common .NET tools.</span></span> <span data-ttu-id="80193-213">ตัวอย่างเช่น คุณสามารถใช้เครื่องมือ [PerfView](https://github.com/Microsoft/perfview) ฟรี</span><span class="sxs-lookup"><span data-stu-id="80193-213">For example, you can use the free [PerfView](https://github.com/Microsoft/perfview) tool.</span></span>

<span data-ttu-id="80193-214">คุณยังสามารถรวบรวมข้อมูลจากรายการคําสั่งได้</span><span class="sxs-lookup"><span data-stu-id="80193-214">You can also collect data from the command line.</span></span> <span data-ttu-id="80193-215">ตัวอย่างเช่น สคริปต์ Windows PowerShell ต่อไปนี้เก็บรวบรวมเวลาการดําเนินการจนกว่าการดําเนินการรูปแบบใด ๆ จะหยุดบนเครื่อง</span><span class="sxs-lookup"><span data-stu-id="80193-215">For example, the following Windows PowerShell script collects the execution time until any format execution is stopped on the machine.</span></span>

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

<span data-ttu-id="80193-216">มีข้อจํากัดบางประการสําหรับวิธีนี้</span><span class="sxs-lookup"><span data-stu-id="80193-216">There are a few limitations to this approach.</span></span> <span data-ttu-id="80193-217">คุณต้องมีสิทธิ์เข้าถึงการจัดการของเครื่อง</span><span class="sxs-lookup"><span data-stu-id="80193-217">You must have administrative access to the machine.</span></span> <span data-ttu-id="80193-218">นอกจากนี้คุณต้องเป็นนักพัฒนาที่มีประสบการณ์ เนื่องจากมีช่วงการเรียนรู้ที่สูงชัน</span><span class="sxs-lookup"><span data-stu-id="80193-218">Additionally, you must be an experienced developer, because there is a steep learning curve.</span></span>

### <a name="making-changes"></a><a name="making-changes"></a><span data-ttu-id="80193-219">การสร้างการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="80193-219">Making changes</span></span>

#### <a name="use-caching"></a><a name="use-caching"></a><span data-ttu-id="80193-220">ใช้การแคช</span><span class="sxs-lookup"><span data-stu-id="80193-220">Use caching</span></span>

<span data-ttu-id="80193-221">แม้ว่าการแคชจะลดระยะเวลาที่จําเป็นในการดึงข้อมูลอีกครั้ง แต่ต้องใช้หน่วยความจํา</span><span class="sxs-lookup"><span data-stu-id="80193-221">Although caching reduces the amount of time that is required to fetch data again, it costs memory.</span></span> <span data-ttu-id="80193-222">ใช้การแคชในกรณีที่จํานวนข้อมูลที่ดึงมาไม่มีขนาดใหญ่มาก</span><span class="sxs-lookup"><span data-stu-id="80193-222">Use caching in cases where the amount of fetched data isn't very large.</span></span> <span data-ttu-id="80193-223">สําหรับข้อมูลเพิ่มเติมและตัวอย่างที่แสดงวิธีการใช้การแคช ให้ดูที่ [ปรับปรุงการแม็ปแบบจําลองตามข้อมูลจากการติดตามการดําเนินการ](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace)</span><span class="sxs-lookup"><span data-stu-id="80193-223">For more information and an example that shows how to use caching, see [Improve the model mapping based on information from the execution trace](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span></span>

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a><span data-ttu-id="80193-224">ใช้ฟิลด์จากการคํานวณที่มีพารามิเตอร์เป็นแคช</span><span class="sxs-lookup"><span data-stu-id="80193-224">Use a cached, parameterized calculated field</span></span>

<span data-ttu-id="80193-225">บางครั้งค่าจะต้องค้นหาซ้ํา ๆ</span><span class="sxs-lookup"><span data-stu-id="80193-225">Sometimes, values must be looked up repeatedly.</span></span> <span data-ttu-id="80193-226">ตัวอย่างเช่น ชื่อบัญชีและหมายเลขบัญชี</span><span class="sxs-lookup"><span data-stu-id="80193-226">Examples include account names and account numbers.</span></span> <span data-ttu-id="80193-227">เพื่อช่วยประหยัดเวลา คุณสามารถสร้างเขตข้อมูลจากการคํานวณที่มีพารามิเตอร์ในระดับบนสุด แล้วเพิ่มฟิลด์ลงในแคช</span><span class="sxs-lookup"><span data-stu-id="80193-227">To help save time, you can create a calculated field that has parameters on the top level, and then add the field to the cache.</span></span>

<span data-ttu-id="80193-228">เราขอแนะนําให้คุณใช้วิธีนี้เฉพาะเมื่อขนาดของข้อมูลที่แคชมีขนาดเล็ก</span><span class="sxs-lookup"><span data-stu-id="80193-228">We recommend that you use this approach only when the size of the cached data is small.</span></span> <span data-ttu-id="80193-229">สําหรับข้อมูลเพิ่มเติม ให้ดูที่ [การปรับปรุงประสิทธิภาพของโซลูชัน ER โดยการเพิ่มแหล่งข้อมูลฟิลด์จากการคํานวณที่มีพารามิเตอร์](er-calculated-field-ds-performance.md)</span><span class="sxs-lookup"><span data-stu-id="80193-229">For more information, see [Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources](er-calculated-field-ds-performance.md).</span></span>

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a><span data-ttu-id="80193-230">ใช้แหล่งข้อมูล JOIN</span><span class="sxs-lookup"><span data-stu-id="80193-230">Use a JOIN data source</span></span>

<span data-ttu-id="80193-231">แหล่งข้อมูล **JOIN** ช่วยให้แบบสอบถามหนึ่งข้อมูลสามารถดึงเรกคอร์ดที่เชื่อมต่อหลายเรกคอร์ดได้</span><span class="sxs-lookup"><span data-stu-id="80193-231">A **JOIN** data source enables several connected records to be fetched by one query.</span></span> <span data-ttu-id="80193-232">แบบสอบถามที่แยกต่างหากไม่จําเป็นต้องถูกใช้เพื่อดึงเรกคอร์ดที่เชื่อมต่อแต่ละเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="80193-232">A separate query doesn't have to be used to fetch each connected record.</span></span> <span data-ttu-id="80193-233">ตัวอย่างเช่น ถ้าคุณมี 1,000 รายการ และคุณนําข้อมูลสินค้าสําหรับแต่ละรายการมาใช้ตามความสัมพันธ์ คุณจะมีการสอบถาม 1,001 รายการ (= 1,000 + 1)</span><span class="sxs-lookup"><span data-stu-id="80193-233">For example, if you have 1,000 lines, and you fetch item data for each line by relation, you will have 1,001 queries (= 1,000 + 1).</span></span> <span data-ttu-id="80193-234">ถ้าคุณใช้แหล่งข้อมูล **JOIN** คุณจะใช้เพียงแบบสอบถามเดียวเพื่อดึงข้อมูลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="80193-234">If you use a **JOIN** data source, you will use only one query to fetch the same data.</span></span> <span data-ttu-id="80193-235">สำหรับข้อมูลเพิ่มเติม ให้ดู [ใช้แหล่งข้อมูล JOIN ในการแม็ปแบบจำลอง ER ในการรับข้อมูลจากหลายตารางแอปพลิเคชัน](er-join-data-sources.md)</span><span class="sxs-lookup"><span data-stu-id="80193-235">For more information, see [Use JOIN data sources in ER model mappings to get data from multiple application tables](er-join-data-sources.md).</span></span>

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a><span data-ttu-id="80193-236">ใช้ฟังก์ชัน FILTER แทนฟังก์ชัน WHERE</span><span class="sxs-lookup"><span data-stu-id="80193-236">Use the FILTER function instead of the WHERE function</span></span>

<span data-ttu-id="80193-237">ฟังก์ชัน **[FILTER](er-functions-list-filter.md)** จะเรียกใช้เงื่อนไขบน SQL Server ในขณะที่ฟังก์ชัน **WHERE** จะดึงข้อมูลทั้งหมดจากรายการ หนึ่งเรกคอร์ดต่อครั้งและใช้เงื่อนไขสําหรับแต่ละเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="80193-237">The **[FILTER](er-functions-list-filter.md)** function runs conditions on SQL Server, whereas the **WHERE** function fetches all data from the list, one record at a time, and applies the condition for each record.</span></span> <span data-ttu-id="80193-238">ตัวอย่างเช่น คุณต้องการเลือกหนึ่งเรกคอร์ดจาก 1,000 เรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="80193-238">For example, you want to select one record out of 1,000 records.</span></span> <span data-ttu-id="80193-239">ถ้าคุณใช้ **WHERE** จะมีการนําเรกคอร์ดทั้งหมด 1,000 เรกคอร์ดมาใช้</span><span class="sxs-lookup"><span data-stu-id="80193-239">If you use **WHERE**, all 1,000 records will be fetched.</span></span> <span data-ttu-id="80193-240">อย่างไรก็ตาม ถ้าคุณใช้ **FILTER** จะมีการนําเรกคอร์ดหนึ่งเรกคอร์ดมาใช้อย่างแน่นอน</span><span class="sxs-lookup"><span data-stu-id="80193-240">However, if you use **FILTER**, exactly one record will be fetched.</span></span> <span data-ttu-id="80193-241">นอกจากนี้ **FILTER** ยังสามารถใช้ดัชนีบนฝั่งฐานข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="80193-241">**FILTER** can also use indexes on the database side.</span></span>

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a><span data-ttu-id="80193-242">การใช้ฟังก์ชันข้อมูลที่รวบรวมหรือแหล่งข้อมูลสะสม</span><span class="sxs-lookup"><span data-stu-id="80193-242">Using collected data functions or an accumulated data data source</span></span>

<span data-ttu-id="80193-243">ถ้าการกําหนดค่าของคุณมีส่วนประกอบ *จัดกลุ่มตาม* ที่สรุปข้อมูลที่ดึงมาก่อนหน้านี้ตามรายงาน ส่วนประกอบจะดึงข้อมูลทั้งหมดอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="80193-243">If your configuration has a *group by* component that summarizes previously fetched data by report, the component will fetch all the data again.</span></span> <span data-ttu-id="80193-244">โดยการใช้ฟังก์ชันข้อมูลที่รวบรวม คุณเปิดใช้งาน ER เพื่อสะสมข้อมูลในระหว่างการนํามาใช้ครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="80193-244">By using collected data functions, you enable ER to accumulate data during the first fetch.</span></span> <span data-ttu-id="80193-245">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกรูปแบบ ER ที่จะทำการตรวจนับและการรวม](tasks/er-format-counting-summing-2.md)</span><span class="sxs-lookup"><span data-stu-id="80193-245">For more information, see [ER Configure format to do counting and summing](tasks/er-format-counting-summing-2.md).</span></span>

#### <a name="rewrite-parts-of-the-configuration-in-x"></a><span data-ttu-id="80193-246">เขียนส่วนของการตั้งค่าคอนฟิกใน X++ ใหม่</span><span class="sxs-lookup"><span data-stu-id="80193-246">Rewrite parts of the configuration in X++</span></span>

<span data-ttu-id="80193-247">ER สนับสนุนวิธีการเรียกของตารางและคลาส รวมถึงส่วนขยาย</span><span class="sxs-lookup"><span data-stu-id="80193-247">ER supports calling methods of tables and classes, including extensions.</span></span> <span data-ttu-id="80193-248">พิจารณาการเขียนส่วนของการแม็ปแบบจําลองใน X++ ใหม่เพื่อช่วยปรับปรุงประสิทธิภาพการทํางาน</span><span class="sxs-lookup"><span data-stu-id="80193-248">Consider rewriting parts of the model mapping in X++ to help improve performance.</span></span>

<span data-ttu-id="80193-249">ER สามารถใช้ข้อมูลจากแหล่งข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="80193-249">ER can consume data from the following sources:</span></span>

- <span data-ttu-id="80193-250">คลาส (แหล่งข้อมูล **ออบเจ็กต์** และ **คลาส**)</span><span class="sxs-lookup"><span data-stu-id="80193-250">Classes (**object** and **class** data sources)</span></span>
- <span data-ttu-id="80193-251">ตาราง (แหล่งข้อมูล **ตาราง** และ **เรกคอร์ดตาราง**)</span><span class="sxs-lookup"><span data-stu-id="80193-251">Tables (**table** and **table records** data sources)</span></span>

<span data-ttu-id="80193-252">นอกจากนี้ [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) ยังมีวิธีการส่งข้อมูลที่คํานวณไว้ล่วงหน้าจากรหัสการเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="80193-252">The [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) also provides a way to send precalculated data from the calling code.</span></span> <span data-ttu-id="80193-253">ชุดแอปพลิเคชันมีตัวอย่างมากมายของวิธีนี้</span><span class="sxs-lookup"><span data-stu-id="80193-253">The application suite contains numerous examples of this approach.</span></span>
