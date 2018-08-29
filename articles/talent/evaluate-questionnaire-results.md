---
title: "ดูและประเมินผลลัพธ์ของแบบสอบถาม"
description: "หัวข้อนี้อธิบายวิธีการดูและประเมินผลลัพธ์ของแบบสอบถามที่ตอบเสร็จสมบูรณ์แล้ว"
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: 9fd4af5589cfab2a92c913639f1192029eb7c592
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---

# <a name="view-and-evaluate-the-results-of-questionnaires"></a><span data-ttu-id="79a01-103">ดูและประเมินผลลัพธ์ของแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="79a01-103">View and evaluate the results of questionnaires</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="79a01-104">หัวข้อนี้อธิบายวิธีการดูและประเมินผลลัพธ์ของแบบสอบถามที่ตอบเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="79a01-104">This topic explains how you can view and evaluate the results of questionnaires that respondents complete.</span></span> 

<span data-ttu-id="79a01-105">หลังจากที่ผู้ตอบได้กรอกข้อมูลแบบสอบถามเสร็จสิ้นแล้ว คุณสามารถดูและประเมินผลลัพธ์ของแบบสอบถามได้หลายวิธี ดังนี้</span><span class="sxs-lookup"><span data-stu-id="79a01-105">After respondents complete a questionnaire, you can view and evaluate the questionnaire results in the following ways:</span></span>

-   <span data-ttu-id="79a01-106">**รอบเวลาคำตอบที่เสร็จสมบูรณ์** – ดูรายละเอียดเกี่ยวกับแบบสอบถามที่ผู้ตอบได้ตอบเสร็จสมบูรณ์แล้ว และสร้างรายงานจะสรุปคำตอบ และคะแนนใด ๆ ที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="79a01-106">**Completed answer sessions** – View details about the questionnaires that respondents have completed, and generate reports to summarize answers and any points that were earned.</span></span>
-   <span data-ttu-id="79a01-107">**กลุ่มผลคะแนน** – ดูรายละเอียดกลุ่มผลคะแนนและสถิติสำหรับแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="79a01-107">**Result groups** – View result group details and statistics for questionnaires.</span></span> <span data-ttu-id="79a01-108">คุณสามารถสร้างสถิติกลุ่มผลคะแนนสำหรับทั้งรอบเวลาคำตอบของแบบสอบถามเดียวหรือรอบเวลาคำตอบทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="79a01-108">Result group statistics can be generated for either a single answer session  of a questionnaire or all answer sessions.</span></span>
-   <span data-ttu-id="79a01-109">**สถิติแบบสอบถาม** – ระบุเกณฑ์การคำนวณสถิติสำหรับกลุ่มของผู้ตอบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="79a01-109">**Questionnaire statistics** – Specify criteria to calculate statistics for a specific group of respondents.</span></span>

<span data-ttu-id="79a01-110">คุณยังสามารถสร้างรายงานต่าง ๆ เพื่อดูผลลัพธ์ที่เรียงลำดับตามบุคคล รอบเวลาคำตอบ หรือกลุ่มผลคะแนน</span><span class="sxs-lookup"><span data-stu-id="79a01-110">You can also generate various reports to view results that are sorted by person, answer session, or result group.</span></span> <span data-ttu-id="79a01-111">รายงานต่อไปนี้เกี่ยวข้องกับแบบสอบถามที่เสร็จสมบูรณ์ต่อไปนี้จะพร้อมใช้งาน:</span><span class="sxs-lookup"><span data-stu-id="79a01-111">The following reports that are related to completed questionnaires are available:</span></span>

-   <span data-ttu-id="79a01-112">คำตอบ</span><span class="sxs-lookup"><span data-stu-id="79a01-112">Answers</span></span>
-   <span data-ttu-id="79a01-113">คำตอบสำหรับแต่ละแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="79a01-113">Answers per questionnaire</span></span>
-   <span data-ttu-id="79a01-114">คำตอบสำหรับแต่ละบุคคล</span><span class="sxs-lookup"><span data-stu-id="79a01-114">Answers per person</span></span>
-   <span data-ttu-id="79a01-115">การวิเคราะห์ผลป้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="79a01-115">Feedback analysis</span></span>

## <a name="answer-session-results"></a><span data-ttu-id="79a01-116">ผลลัพธ์รอบเวลาของคำตอบ</span><span class="sxs-lookup"><span data-stu-id="79a01-116">Answer session results</span></span>
<span data-ttu-id="79a01-117">หลังจากที่ผู้ตอบแบบสอบถามตอบแบบสอบถามแล้ว คุณสามารถดูผลลัพธ์ของรอบเวลาคำตอบที่เสร็จสมบูรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="79a01-117">After respondents complete a questionnaire, you can view the results of the completed answer sessions.</span></span> <span data-ttu-id="79a01-118">รอบเวลาคำตอบเป็นการตอบสนองของผู้ใช้หนึ่งรายต่อบแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="79a01-118">An answer session is one user’s response to a questionnaire.</span></span> <span data-ttu-id="79a01-119">คุณสามารถดูรายละเอียดเกี่ยวกับรอบเวลาคำตอบที่เสร็จสมบูรณ์บนหน้า **คำตอบ** ได้</span><span class="sxs-lookup"><span data-stu-id="79a01-119">You can view details about completed answer sessions on the **Answers** page.</span></span> <span data-ttu-id="79a01-120">รอบเวลาคำตอบที่รวมอยู่ในหน้า **คำตอบ** จะถูกกรองข้อมูลในลักษณะต่าง ๆ ขึ้นอยู่กับว่าคุณเปิดหน้าอย่างไร:</span><span class="sxs-lookup"><span data-stu-id="79a01-120">The answer sessions that are included on the **Answers** page are filtered in various ways, depending on how you open the page:</span></span>

-   <span data-ttu-id="79a01-121">แบบสอบถามทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="79a01-121">All questionnaires</span></span>
-   <span data-ttu-id="79a01-122">แบบสอบถามที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="79a01-122">A specific questionnaire</span></span>
-   <span data-ttu-id="79a01-123">บุคคลที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="79a01-123">A specific person</span></span>

<span data-ttu-id="79a01-124">จากหน้า **คำตอบ** คุณสามารถดูรายละเอียดเกี่ยวกับคำตอบ คะแนนที่ได้รับ คำตอบของผู้ตอบในกลุ่มผลคะแนน และลำดับชั้นของคำถามที่ใช้ในแบบสอบถามที่เลือก ถ้ามีการใช้ลำดับชั้นของคำถาม ได้</span><span class="sxs-lookup"><span data-stu-id="79a01-124">From the **Answers** page, you can view details about answers, points that were earned, a respondent’s responses in each result group, and the question hierarchy that was used on the selected questionnaire, if a question hierarchy was used.</span></span> <span data-ttu-id="79a01-125">คุณยังสามารถสร้างและพิมพ์รายงานต่อไปนี้ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="79a01-125">You can also generate and print the following reports:</span></span>

-   <span data-ttu-id="79a01-126">**ผลลัพธ์ของรายงาน** – รายงานนี้แสดงภาพของคะแนนที่ได้รับสำหรับแต่ละกลุ่มผลคะแนนสำหรับรอบเวลาคำตอบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="79a01-126">**Results report** – This report shows a graphical representation of the points that were earned per result group for the selected answer session.</span></span>
-   <span data-ttu-id="79a01-127">**รายงานคำตอบ** – รายงานนี้แสดงคำตอบที่ผู้ตอบเลือกสำหรับแต่ละคำถามในแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="79a01-127">**Answer report** – This report shows the answers that the respondent selected for each question on the questionnaire.</span></span>
-   <span data-ttu-id="79a01-128">**คำตอบไม่ถูกต้อง** – รายงานนี้แสดงข้อมูลที่เกี่ยวข้องกับคำตอบที่ไม่ถูกต้องที่ผู้ตอบเลือก</span><span class="sxs-lookup"><span data-stu-id="79a01-128">**Incorrect answers** – This report shows information that is related to the incorrect answers that the respondent selected.</span></span>

<span data-ttu-id="79a01-129">**หมายเหตุ:** รายงาน **ผลลัพธ์** จะพร้อมใช้เฉพาะเมื่อคุณใช้กลุ่มผลลัพธ์ในแบบสอบถาม และ ถ้าคุณเลือก **หน้าผลลัพธ์** ในหน้า **แบบสอบถาม** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="79a01-129">**Note:** The **Results** report is available only if you use results groups on the questionnaire, and if you selected **Results page** on the **Questionnaires** page.</span></span> <span data-ttu-id="79a01-130">รายงาน **คำตอบ** และรายงาน **คำตอบไม่ถูกต้อง** จะพร้อมใช้เฉพาะเมื่อคุณเลือก **รายงานคำตอบ** บนหน้า **แบบสอบถาม** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="79a01-130">The **Answer** report and the **Incorrect answers** report are available only if you selected **Answer report** on the **Questionnaires** page.</span></span>

## <a name="questionnaire-statistics"></a><span data-ttu-id="79a01-131">สถิติแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="79a01-131">Questionnaire statistics</span></span>
<span data-ttu-id="79a01-132">คุณสามารถใช้สถิติแบบสอบถามเพื่อวิเคราะห์ผลลัพธ์ของแบบสอบถามเสร็จสมบูรณ์ ขึ้นอยู่กับการคำนวณที่คุณกำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="79a01-132">You can use questionnaire statistics to analyze the results of a completed questionnaire, based on calculations that you define.</span></span> <span data-ttu-id="79a01-133">เมื่อต้องการกำหนดการคำนวณ คุณต้องดำเนินการงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="79a01-133">To define calculations, you must complete the following tasks:</span></span>

-   <span data-ttu-id="79a01-134">เลือกเกณฑ์การคำนวณ และแสดงสถิติ</span><span class="sxs-lookup"><span data-stu-id="79a01-134">Select criteria to calculate and display the statistics.</span></span>
    -   <span data-ttu-id="79a01-135">คุณสามารถแสดงสถิติตามแบบสอบถาม คำถาม แถวคำถาม หรือกลุ่มผลคะแนน</span><span class="sxs-lookup"><span data-stu-id="79a01-135">You can show statistics by questionnaire, questions, question rows, or results groups.</span></span>
    -   <span data-ttu-id="79a01-136">เลือกชนิดของแผนภูมิที่จะใช้เมื่อคุณดูผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="79a01-136">Select the type of chart that will be used when you view results.</span></span>
    -   <span data-ttu-id="79a01-137">เลือกชนิดของบุคคลจากเครือข่าย เช่น พนักงาน ผู้ติดต่อ หรือผู้สมัคร เพื่อรวมคำตอบ</span><span class="sxs-lookup"><span data-stu-id="79a01-137">Select the types of people from the network, such as employees, contact persons, or applicants, to include answers for.</span></span> <span data-ttu-id="79a01-138">คุณยังสามารถรวมคำตอบจากแบบสอบถามที่ตอบโดยไม่ระบุชื่อ</span><span class="sxs-lookup"><span data-stu-id="79a01-138">You can also include answers from questionnaires that were completed anonymously.</span></span>
    -   <span data-ttu-id="79a01-139">ตั้งค่าช่วงเวลาที่ขึ้นอยู่กับอายุหรือความอาวุโสเพื่อวิเคราะห์ผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="79a01-139">Set up intervals that are based on age or seniority to analyze results.</span></span>
-   <span data-ttu-id="79a01-140">เลือกหรือตรวจสอบการตั้งค่าที่ปรับปรุงชื่อเรื่องของสถิติ</span><span class="sxs-lookup"><span data-stu-id="79a01-140">Select or verify settings that refine the subject of the statistics.</span></span> <span data-ttu-id="79a01-141">ตัวอย่างเช่น โดยการเลือกรหัสไปรษณีย์ คุณสามารถวิเคราะห์ผลลัพธ์สำหรับผู้ตอบทั้งหมดภายในพื้นที่ทางภูมิศาสตร์ที่ระบุได้</span><span class="sxs-lookup"><span data-stu-id="79a01-141">For example, by selecting a ZIP Code or postal code, you can analyze results for all respondents within a specific geographic area.</span></span>
-   <span data-ttu-id="79a01-142">เลือกหรือตรวจสอบเงื่อนไขในการวิเคราะห์ผลลัพธ์ตามลักษณะของผู้ตอบหรือแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="79a01-142">Select or verify criteria to analyze results by respondent or questionnaire characteristics.</span></span> <span data-ttu-id="79a01-143">ตัวอย่างเช่น โดยการเลือก **รหัสไปรษณีย์** คุณสามารถวิเคราะห์ความสัมพันธ์ระหว่างสถานที่อยู่ของผู้ตอบและคำตอบที่ถูกต้องได้</span><span class="sxs-lookup"><span data-stu-id="79a01-143">For example, by selecting **ZIP/postal code**, you can analyze the correlation between a respondent’s location and correct answers.</span></span>

<span data-ttu-id="79a01-144">ระบบจะบันทึกการตั้งค่าที่คุณกำหนด และคุณสามารถใช้การตั้งค่านั้นเพื่อคำนวณผลลัพธ์ใหม่เป็นระยะๆ ได้</span><span class="sxs-lookup"><span data-stu-id="79a01-144">The settings that you define are saved and can be used to periodically recalculate results.</span></span>

<a name="additional-resources"></a><span data-ttu-id="79a01-145">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="79a01-145">Additional resources</span></span>
--------

[<span data-ttu-id="79a01-146">การออกแบบแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="79a01-146">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="79a01-147">โดยใช้แบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="79a01-147">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="79a01-148">การแจกจ่ายและการตอบแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="79a01-148">Distributing and completing questionnaires</span></span>](distribute-questionnaires.md)


