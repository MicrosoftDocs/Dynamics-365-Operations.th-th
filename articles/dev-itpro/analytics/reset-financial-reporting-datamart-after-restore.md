---
title: "รีเซ็ต Data Mart การรายงานทางการเงิน"
description: "หัวข้อนี้อธิบายวิธีการรีเซ็ต Data Mart การรายงานทางการเงิน"
author: aolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 0786d3377b914791106ef30455d676e5ab2ae03d
ms.openlocfilehash: c708fa18b8676d8ff57c26b3176a36d86df29387
ms.contentlocale: th-th
ms.lasthandoff: 12/07/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a><span data-ttu-id="46d7b-103">รีเซ็ต Data Mart การรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="46d7b-103">Reset the Financial reporting data mart</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="46d7b-104">หัวข้อนี้อธิบายวิธีการรีเซ็ต Data Mart การรายงานทางการเงินสำหรับรุ่นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="46d7b-104">This topic explains how to reset the Financial reporting data mart for the following versions:</span></span>

- <span data-ttu-id="46d7b-105">Microsoft Dynamics 365 for Finance and Operations: Financial reporting รุ่น 7.2.6.0 และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="46d7b-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>
- <span data-ttu-id="46d7b-106">Microsoft Dynamics 365 for Finance and Operations: Financial reporting รุ่น 7.0.10000.4 และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="46d7b-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>
- <span data-ttu-id="46d7b-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (แบบ On-premises)</span><span class="sxs-lookup"><span data-stu-id="46d7b-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises)</span></span>

<span data-ttu-id="46d7b-108">เพื่อรับการรายงานทางการเงินของ Finance and Operations รุ่น 7.2.6.0 คุณสามารถดาวน์โหลด KB 4052514 ได้จาก <https://support.microsoft.com/en-us/help/4052514></span><span class="sxs-lookup"><span data-stu-id="46d7b-108">To get Finance and Operations Financial reporting release 7.2.6.0, you can download KB 4052514 from <https://support.microsoft.com/en-us/help/4052514>.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a><span data-ttu-id="46d7b-109">รีเซ็ต Data Mart การรายงานทางการเงิน สำหรับการรายงานทางการเงินของ Finance and Operations รุ่น 7.2.6.0 และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="46d7b-109">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a><span data-ttu-id="46d7b-110">รีเซ็ตData Mart การรายงานทางการเงินจากตัวออกแบบรายงาน</span><span class="sxs-lookup"><span data-stu-id="46d7b-110">Reset the Financial reporting data mart from Report designer</span></span>

> [!NOTE]
> <span data-ttu-id="46d7b-111">ขั้นตอนในกระบวนการนี้จะได้รับการสนับสนุนสำหรับการรายงานทางการเงินของ Finance and Operations รุ่น 7.2.6.0 และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="46d7b-111">The steps in this process are supported for Finance and Operations Financial reporting release 7.2.6.0 and later.</span></span> <span data-ttu-id="46d7b-112">ถ้าคุณมีรุ่นก่อนหน้า ติดต่อทีมงานฝ่ายสนับสนุนเพื่อขอความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="46d7b-112">If you have an earlier release, contact the Support team for assistance.</span></span>

<span data-ttu-id="46d7b-113">ในสถานการณ์เฉพาะ คุณอาจต้องรีเซ็ต data mart สำหรับการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="46d7b-113">In specific scenarios, you might have to reset the data mart for Financial reporting.</span></span> <span data-ttu-id="46d7b-114">คุณสามารถทำงานนี้ให้สำเร็จได้ในไคลเอนต์ตัวออกแบบรายงาน</span><span class="sxs-lookup"><span data-stu-id="46d7b-114">You can complete this task in the Report designer client.</span></span> <span data-ttu-id="46d7b-115">นี่คือบางสถานการณ์ที่คุณอาจต้องรีเซ็ต data mart:</span><span class="sxs-lookup"><span data-stu-id="46d7b-115">Here are some scenarios where you might have to reset the data mart:</span></span>

- <span data-ttu-id="46d7b-116">มีการคืนค่าฐานข้อมูล Finance and Operations แต่ไม่ได้รับการคืนค่าฐานข้อมูล data mart</span><span class="sxs-lookup"><span data-stu-id="46d7b-116">The Finance and Operations database was restored, but the data mart database wasn't restored.</span></span>
- <span data-ttu-id="46d7b-117">คุณจะเห็นข้อมูลที่ไม่ถูกต้องสำหรับรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="46d7b-117">You see incorrect data for a period.</span></span>
- <span data-ttu-id="46d7b-118">การสนับสนุนแนะนำให้คุณรีเซ็ต data mart เนื่องจากเป็นส่วนหนึ่งของขั้นตอนการแก้ไขปัญหาเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="46d7b-118">Support instructs you to reset the data mart as part of a troubleshooting step.</span></span>

<span data-ttu-id="46d7b-119">การรีเซ็ต data mart ควรเสร็จสิ้นในระหว่างเวลาที่จำนวนของการประมวลผลในฐานข้อมูลมีขนาดเล็กเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="46d7b-119">The data mart reset should be done only during times when the amount of processing on the database is small.</span></span> <span data-ttu-id="46d7b-120">รายงานทางการเงินจะไม่พร้อมใช้งานในระหว่างกระบวนการตั้งค่าใหม่</span><span class="sxs-lookup"><span data-stu-id="46d7b-120">Financial reporting will be unavailable during the reset process.</span></span>

#### <a name="reset-the-data-mart"></a><span data-ttu-id="46d7b-121">รีเซ็ต data mart</span><span class="sxs-lookup"><span data-stu-id="46d7b-121">Reset the data mart</span></span>

<span data-ttu-id="46d7b-122">เพื่อรีเซ็ต data mart ในตัวออกแบบรายงาน บนเมนู **เครื่องมือ** เลือก **รีเซ็ต Data Mart**</span><span class="sxs-lookup"><span data-stu-id="46d7b-122">To reset the data mart, in Report designer, on the **Tools** menu, select **Reset Data Mart**.</span></span> <span data-ttu-id="46d7b-123">กล่องโต้ตอบที่ปรากฏมีสองส่วน: **สถิติ** และ **รีเซ็ต**</span><span class="sxs-lookup"><span data-stu-id="46d7b-123">The dialog box that appears has two sections: **Statistics** and **Reset**.</span></span>

<span data-ttu-id="46d7b-124">[![รีเซ็ตกล่องโต้ตอบ Data Mart](./media/Statistics.png)](./media/Statistics.png)</span><span class="sxs-lookup"><span data-stu-id="46d7b-124">[![Reset Data Mart dialog box](./media/Statistics.png)](./media/Statistics.png)</span></span>

##### <a name="integration-attempts"></a><span data-ttu-id="46d7b-125">ความพยายามในการรวม</span><span class="sxs-lookup"><span data-stu-id="46d7b-125">Integration attempts</span></span>

<span data-ttu-id="46d7b-126">กริด **ความพยายามในการรวม** แสดงจำนวนครั้งที่ระบบได้พยายามที่จะรวมธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="46d7b-126">The **Integration attempts** grid shows how many times the system has tried to integrate transactions.</span></span> <span data-ttu-id="46d7b-127">ระบบพยายามที่จะรวมข้อมูลตลอดรอบระยะเวลาของวันต่อไป ถ้าความพยายามสองสามครั้งแรกไม่ประสบความสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="46d7b-127">The system continues to try to integrate data over a period of days if the first few attempts aren't successful.</span></span> <span data-ttu-id="46d7b-128">คุณจะทราบว่า data mart ต้องถูกรีเซ็ต ถ้าจำนวนครั้งของความพยายามคือ อย่างน้อย 8 ครั้ง และถ้ามีชุดมิติหรือเรกคอร์ดธุรกรรมจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="46d7b-128">You will know that the data mart must be reset is if the number of attempts is 8 or more, and if there are many Dimension combination or Transaction records.</span></span> <span data-ttu-id="46d7b-129">ในสถานการณ์นี้ ข้อมูลจะไม่ถูกรายงาน</span><span class="sxs-lookup"><span data-stu-id="46d7b-129">In this situation, the data won't be reported on.</span></span>

##### <a name="data-status"></a><span data-ttu-id="46d7b-130">สถานะของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="46d7b-130">Data status</span></span>

<span data-ttu-id="46d7b-131">กริด **สถานะของข้อมูล** จะแสดงสแนปช็อตของธุรกรรม อัตราแลกเปลี่ยน และค่ามิติใน data mart</span><span class="sxs-lookup"><span data-stu-id="46d7b-131">The **Data status** grid provides a snapshot of the transactions, exchange rates, and dimension values in the data mart.</span></span> <span data-ttu-id="46d7b-132">เรกคอร์ดที่ล้าสมัยจำนวนมากบ่งชี้ว่า มีการอัพเดตจำนวนมากไปยังเรกคอร์ดเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="46d7b-132">A large number of stale records indicates that numerous updates to the records have occurred.</span></span> <span data-ttu-id="46d7b-133">สถานการณ์นี้อาจทำให้เวลาในการสร้างรายงานช้าลง</span><span class="sxs-lookup"><span data-stu-id="46d7b-133">This situation might cause slower report generation times.</span></span>

##### <a name="misaligned-main-account-categories"></a><span data-ttu-id="46d7b-134">ประเภทบัญชีหลักที่ไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="46d7b-134">Misaligned main account categories</span></span>

<span data-ttu-id="46d7b-135">ถ้าคุณกำลังใช้รุ่นที่เก่ากว่าการรายงานทางการเงินของ Microsoft Dynamics 365 for Finance and Operations รุ่น7.2.1 คุณอาจต้องรีเซ็ต data mart ถ้าคุณเปลี่ยนชื่อบัญชี และย้ายบัญชีระหว่างประเภทบัญชี</span><span class="sxs-lookup"><span data-stu-id="46d7b-135">If you're using a release that is earlier than Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.1, you might have to reset the data mart if you rename accounts and move accounts between account categories.</span></span> <span data-ttu-id="46d7b-136">การดำเนินการเหล่านี้อาจทำให้ประเภทบัญชีหลักกลายเป็นไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="46d7b-136">These actions can cause main account categories to become misaligned.</span></span> <span data-ttu-id="46d7b-137">ฟิลด์ **ประเภทบัญชีหลักที่ไม่สอดคล้องกัน** แสดงว่าคุณประสบกับปัญหานั้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="46d7b-137">The **Misaligned main account categories** field shows whether you're experiencing that issue.</span></span>

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a><span data-ttu-id="46d7b-138">รีเซ็ต data mart ในการรายงานทางการเงินสำหรับ Finance and Operations รุ่น 7.2.6.0</span><span class="sxs-lookup"><span data-stu-id="46d7b-138">Reset the data mart in Finance and Operations Financial reporting release 7.2.6.0</span></span>

<span data-ttu-id="46d7b-139">เพื่อรีเซ็ต data mart ในการรายงานทางการเงินสำหรับ Finance and Operations รุ่น 7.2.6.0 และรุ่นก่อนหน้า ในกล่องโต้ตอบ **รีเซ็ต Data Mart** เลือกกล่องกาเครื่องหมาย **รีเซ็ต data mart** และจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="46d7b-139">To reset the data mart in Finance and Operations Financial reporting release 7.2.6.0 and earlier, in the **Reset Data Mart** dialog box, select the **Reset data mart** check box, and then select **OK**.</span></span> <span data-ttu-id="46d7b-140">คุณควรรีเซ็ต data mart ในระหว่างการหยุดทำงานตามกำหนดการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="46d7b-140">You should reset the data mart only during scheduled downtime.</span></span>

<span data-ttu-id="46d7b-141">[![รีเซ็ตกล่องโต้ตอบ Data Mart](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="46d7b-141">[![Reset data mart check box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a><span data-ttu-id="46d7b-142">รีเซ็ต data mart และเลือกเหตุผลในการรายงานทางการเงินสำหรับ Microsoft Dynamics 365 for Finance and Operations รุ่น 7.3.0</span><span class="sxs-lookup"><span data-stu-id="46d7b-142">Reset the data mart and select a reason in Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.3.0</span></span>

<span data-ttu-id="46d7b-143">ถ้าคุณกำหนดว่าการรีเซ็ต data mart จำเป็น ให้เลือกกล่องกาเครื่องหมาย **รีเซ็ต data mart** และจากนั้น เลือกเหตุผลในฟิลด์ **เหตุผล**</span><span class="sxs-lookup"><span data-stu-id="46d7b-143">If you determine that a data mart reset is required, select the **Reset data mart** check box, and then select a reason in the **Reason** field.</span></span> <span data-ttu-id="46d7b-144">โดยตัวเลือกที่คุณสามารถเลือกได้มีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="46d7b-144">The following options are available:</span></span>

- <span data-ttu-id="46d7b-145">**ข้อมูลที่ขาดหายไปหรือไม่ถูกต้อง** – ขึ้นอยู่กับสถิติ คุณได้กำหนดว่าข้อมูลอาจหายไป</span><span class="sxs-lookup"><span data-stu-id="46d7b-145">**Missing or incorrect data** – Based on the statistics, you've determined that data might be missing.</span></span> <span data-ttu-id="46d7b-146">ก่อนที่คุณดำเนินการต่อ เราขอแนะนำให้คุณทำงานกับฝ่ายสนับสนุนเพื่อกำหนดสาเหตุราก</span><span class="sxs-lookup"><span data-stu-id="46d7b-146">Before you continue, we recommend that you work with Support to determine the root cause.</span></span>
- <span data-ttu-id="46d7b-147">**คืนค่าฐานข้อมูล** – มีการคืนค่าฐานข้อมูล Finance and Operations แต่ไม่มีการคืนค่าฐานข้อมูล สำหรับ data mart ของการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="46d7b-147">**Restore database** – The Finance and Operations database was restored, but the database for the Financial reporting data mart wasn't restored.</span></span>
- <span data-ttu-id="46d7b-148">**อื่น ๆ** – คุณกำลังรีเซ็ต data mart เพราะเหตุผลอื่น</span><span class="sxs-lookup"><span data-stu-id="46d7b-148">**Other** – You're resetting the data mart for another reason.</span></span> <span data-ttu-id="46d7b-149">ถ้าคุณเป็นกังวลว่าจะมีปัญหา ติดต่อฝ่ายสนับสนุนเพื่อระบุปัญหา</span><span class="sxs-lookup"><span data-stu-id="46d7b-149">If you're concerned that there is an issue, contact Support to identify it.</span></span>

> [!NOTE]
> <span data-ttu-id="46d7b-150">ตรวจสอบว่างานที่มีอยู่ทั้งหมดเสร็จสิ้น ก่อนที่คุณดำเนินขั้นตอนต่างๆ จนเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="46d7b-150">Verify that all existing tasks have finished integrating before you complete the steps.</span></span> <span data-ttu-id="46d7b-151">คุณสามารถดูสถานะของการรวมได้ ด้วยการเลือก **เครื่องมือ** &gt; **สถานะการรวม**</span><span class="sxs-lookup"><span data-stu-id="46d7b-151">You can view the status of the integration by selecting **Tools** &gt; **Integration status**.</span></span>

#### <a name="clear-users-and-companies"></a><span data-ttu-id="46d7b-152">ล้างผู้ใช้และบริษัท</span><span class="sxs-lookup"><span data-stu-id="46d7b-152">Clear users and companies</span></span>

<span data-ttu-id="46d7b-153">เลือกกล่องกาเครื่องหมาย **ล้างผู้ใช้และบริษัท** ถ้าคุณคืนค่าฐานข้อมูลของคุณ แต่จากนั้นคุณได้ทำการเปลี่ยนแปลงไปยังผู้ใช้หรือบริษัท</span><span class="sxs-lookup"><span data-stu-id="46d7b-153">Select the **Clear users and companies** check box if you restored your database, but you then made changes to users or companies.</span></span> <span data-ttu-id="46d7b-154">คุณแทบจะไม่ต้องเลือกกล่องกาเครื่องหมายนี้เลย</span><span class="sxs-lookup"><span data-stu-id="46d7b-154">You should rarely have to select this check box.</span></span>

<span data-ttu-id="46d7b-155">เมื่อคุณพร้อมที่จะเริ่มต้นกระบวนการรีเซ็ต เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="46d7b-155">When you're ready to start the reset process, select **OK**.</span></span> <span data-ttu-id="46d7b-156">คุณได้รับพร้อมท์ให้ยืนยันว่า คุณพร้อมที่จะเริ่มต้นกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="46d7b-156">You're prompted to confirm that you're ready to start the process.</span></span> <span data-ttu-id="46d7b-157">โปรดทราบว่า การรายงานทางการเงินจะไม่พร้อมใช้งานในระหว่างการรีเซ็ต และการรวมข้อมูลเริ่มต้นที่เกิดขึ้นในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="46d7b-157">Note that Financial reporting won't be available during the reset and the initial data integration that occurs afterward.</span></span>

<span data-ttu-id="46d7b-158">ถ้าคุณต้องการตรวจสอบสถานะของการรวม เลือก **เครื่องมือ** &gt; **สถานะการรวม** เพื่อดูครั้งล่าสุดที่การรวมถูกเรียกใช้และสถานะ</span><span class="sxs-lookup"><span data-stu-id="46d7b-158">If you want to review the status of the integration, select **Tools** &gt; **Integration status** to see the last time that the integration was run and the status.</span></span>

<span data-ttu-id="46d7b-159">[![ดูสถานะของการรวม](./media/Integration.png)](./media/Integration.png)</span><span class="sxs-lookup"><span data-stu-id="46d7b-159">[![View the status of the integration](./media/Integration.png)](./media/Integration.png)</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a><span data-ttu-id="46d7b-160">รีเซ็ต Data Mart ของการรายงานทางการเงินสำหรับการรายงานทางการเงินของ Finance and Operations รุ่น 7.0.10000.4 และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="46d7b-160">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>

<span data-ttu-id="46d7b-161">ถ้าคุณเคยคืนค่าฐานข้อมูล Finance and Operations ของคุณจากการสำรองข้อมูล หรือคัดลอกฐานข้อมูลจากสภาพแวดล้อมอื่น คุณต้องทำตามขั้นตอนในส่วนนี้ เพื่อช่วยรับรองว่า Data Mart การรายงานทางการเงินใช้ฐานข้อมูล Finance and Operations ที่คืนค่าได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="46d7b-161">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this section to help guarantee that the Financial reporting data mart correctly uses the restored Finance and Operations database.</span></span>

> [!NOTE]
> <span data-ttu-id="46d7b-162">ขั้นตอนในกระบวนการนี้ได้รับการสนับสนุนสำหรับแอพลิเคชัน Microsoft Dynamics รุ่น 7.0.1 (พฤษภาคม 2016) (การสร้างแอพลิเคชัน 7.0.1265.23014 และการสร้างการรายงานทางการเงิน 7.0.10000.4) และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="46d7b-162">The steps in this process are supported for Microsoft Dynamics AX application version 7.0.1 (May 2016) (application build 7.0.1265.23014 and Financial reporting build 7.0.10000.4) and later.</span></span> <span data-ttu-id="46d7b-163">ถ้าคุณมี Finance and Operations รุ่นก่อนหน้า ให้ติดต่อทีมสนับสนุนของเราสำหรับความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="46d7b-163">If you have an earlier version of Finance and Operations, contact Support for assistance.</span></span>

### <a name="export-report-definitions"></a><span data-ttu-id="46d7b-164">ส่งออกข้อกำหนดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="46d7b-164">Export report definitions</span></span>

<span data-ttu-id="46d7b-165">ลำดับแรก ให้ทำตามขั้นตอนเหล่านี้เพื่อส่งออกแบบรายงานจากตัวออกแบบรายงาน</span><span class="sxs-lookup"><span data-stu-id="46d7b-165">First, follow these steps to export the report designs from Report designer.</span></span>

1. <span data-ttu-id="46d7b-166">ในตัวออกแบบรายงาน เลือก **บริษัท** &gt; **กลุ่มบล็อคส่วนประกอบ**</span><span class="sxs-lookup"><span data-stu-id="46d7b-166">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="46d7b-167">เลือกกลุ่มบล็อคส่วนประกอบที่จะส่งออก และจากนั้นเลือก **ส่งออก**</span><span class="sxs-lookup"><span data-stu-id="46d7b-167">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="46d7b-168">สำหรับ Finance and Operations สนับสนุนกลุ่มบล็อคส่วนประกอบเพียงหนึ่งรายการเท่านั้น **ค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="46d7b-168">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="46d7b-169">เลือกข้อกำหนดของรายงานที่จะส่งออก:</span><span class="sxs-lookup"><span data-stu-id="46d7b-169">Select the report definitions to export:</span></span>

    - <span data-ttu-id="46d7b-170">หากต้องการส่งออกข้อกำหนดของรายงานและบล็อคส่วนประกอบที่เกี่ยวข้องทั้งหมดของคุณ เลือก **เลือกทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="46d7b-170">To export all your report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="46d7b-171">เมื่อต้องการส่งออกรายงาน แถว คอลัมน์ แผนภูมิ หรือชุดมิติเฉพาะ เลือกแท็บที่เหมาะสม และจากนั้นเลือกรายการที่จะส่งออก</span><span class="sxs-lookup"><span data-stu-id="46d7b-171">To export specific reports, rows, columns, trees, or dimension sets, select the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="46d7b-172">กดปุ่ม Ctrl และค้างไว้ เพื่อเลือกหลายรายการบนแท็บ เมื่อคุณเลือกรายงานที่จะส่งออก แถว คอลัมน์ ลำดับ หรือชุดมิติที่เกี่ยวข้อง จะถูกเลือกด้วย</span><span class="sxs-lookup"><span data-stu-id="46d7b-172">Press and hold the Ctrl key to select multiple items on a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4. <span data-ttu-id="46d7b-173">เลือก **ส่งออก**</span><span class="sxs-lookup"><span data-stu-id="46d7b-173">Select **Export**.</span></span>
5. <span data-ttu-id="46d7b-174">ป้อนชื่อไฟล์ และเลือกตำแหน่งที่ปลอดภัยที่คุณต้องการบันทึกข้อกำหนดของรายงานที่ส่งออก</span><span class="sxs-lookup"><span data-stu-id="46d7b-174">Enter a file name, and select a secure location where you want to save the exported report definitions.</span></span>
6. <span data-ttu-id="46d7b-175">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="46d7b-175">Select **Save**.</span></span>

<span data-ttu-id="46d7b-176">คุณสามารถคัดลอกหรืออัปโหลดไฟล์ไปยังตำแหน่งที่ปลอดภัยได้</span><span class="sxs-lookup"><span data-stu-id="46d7b-176">You can copy or upload the file to a secure location.</span></span> <span data-ttu-id="46d7b-177">ในวิธีนี้ ไฟล์สามารถถูกนำเข้าลงในสภาพแวดล้อมที่แตกต่างกันในภายหลังได้</span><span class="sxs-lookup"><span data-stu-id="46d7b-177">In this way, the file can be imported into a different environment later.</span></span> <span data-ttu-id="46d7b-178">สำหรับข้อมูลเกี่ยวกับวิธีใช้บัญชีการจัดเก็บ Microsoft Azure ดู [ถ่ายโอนข้อมูลโดยใช้ยูทิลิตี้บรรทัดคำสั่ง AzCopy](/azure/storage/storage-use-azcopy)</span><span class="sxs-lookup"><span data-stu-id="46d7b-178">For information about how to use a Microsoft Azure storage account, see [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span>

> [!NOTE]
> <span data-ttu-id="46d7b-179">Microsoft ไม่ได้ให้บัญชีการจัดเก็บ เนื่องจากเป็นส่วนหนึ่งของข้อตกลงของ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="46d7b-179">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="46d7b-180">คุณต้องซื้อบัญชีการจัดเก็บหรือใช้บัญชีการจัดเก็บจากการสมัครใช้งาน Azure ที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="46d7b-180">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span>

> [!WARNING]
> <span data-ttu-id="46d7b-181">ระวังลักษณะการทำงานของไดรฟ์ D บนเครื่องเสมือนของ Azure (VMs)</span><span class="sxs-lookup"><span data-stu-id="46d7b-181">Be aware of the behavior of drive D on Azure virtual machines (VMs).</span></span> <span data-ttu-id="46d7b-182">ห้ามจัดเก็บกลุ่มบล็อคส่วนประกอบที่ส่งออกของคุณอย่างถาวรบนไดรฟ์ D สำหรับข้อมูลเพิ่มเติมเกี่ยวกับไดรฟ์ชั่วคราว ดู [การทำความเข้าใจไดรฟ์ชั่วคราวบน Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/)</span><span class="sxs-lookup"><span data-stu-id="46d7b-182">Don't permanently store your exported building block groups on drive D. For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

### <a name="stop-services"></a><span data-ttu-id="46d7b-183">หยุดการบริการ</span><span class="sxs-lookup"><span data-stu-id="46d7b-183">Stop services</span></span>

<span data-ttu-id="46d7b-184">บริการ Microsoft Windows ต่อไปนี้จะมีการเชื่อมต่อแบบเปิดกับฐานข้อมูล Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="46d7b-184">The following Microsoft Windows services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="46d7b-185">ดังนั้น คุณต้องใช้ Microsoft Remote Desktop ในการเชื่อมต่อกับคอมพิวเตอร์ทั้งหมดในสภาพแวดล้อม และจากนั้นใช้ services.msc เพื่อหยุดการบริการเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="46d7b-185">Therefore, you must use Microsoft Remote Desktop to connect to all the computers in the environment and then use services.msc to stop these services.</span></span>

- <span data-ttu-id="46d7b-186">บริการเผยแพร่เวิลด์ไวด์เว็บ (บนคอมพิวเตอร์ Application Object Servers [AOS] ทั้งหมด)</span><span class="sxs-lookup"><span data-stu-id="46d7b-186">World wide web publishing service (on all Application Object Servers [AOS] computers)</span></span>
- <span data-ttu-id="46d7b-187">การจัดการชุดงานของ Microsoft Dynamics 365 for Finance and Operations (บนคอมพิวเตอร์ AOS ที่ไม่ใช่แบบส่วนตัวเท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="46d7b-187">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="46d7b-188">บริการประมวลผลของ Management Reporter 2012 (บนคอมพิวเตอร์ข่าวกรองธุรกิจ [BI] เท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="46d7b-188">Management Reporter 2012 Process Service (on Business intelligence [BI] computers only)</span></span>

### <a name="reset"></a><span data-ttu-id="46d7b-189">รีเซ็ต</span><span class="sxs-lookup"><span data-stu-id="46d7b-189">Reset</span></span>

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="46d7b-190">ดาวน์โหลดแพคเกจ MinorVersionDataUpgrade.zip ล่าสุด</span><span class="sxs-lookup"><span data-stu-id="46d7b-190">Download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="46d7b-191">ดาวน์โหลดแพคเกจ MinorVersionDataUpgrade.zip ล่าสุด</span><span class="sxs-lookup"><span data-stu-id="46d7b-191">Download the latest MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="46d7b-192">สำหรับคำแนะนำเกี่ยวกับวิธีการค้นหาและดาวน์โหลดรุ่นที่ถูกต้องของแพคเกจการอัพเกรดข้อมูล ดู[ดาวน์โหลดแพคเกจสามารถปรับใช้ได้ในการอัพเกรดข้อมูลล่าสุด](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages)</span><span class="sxs-lookup"><span data-stu-id="46d7b-192">For instructions about how to find and download the correct version of the data upgrade package, see the[Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span></span> <span data-ttu-id="46d7b-193">ไม่จำเป็นต้องอัพเกรดเพื่อที่จะดาวน์โหลดแพคเกจ MinorVersionDataUpgrade.zip</span><span class="sxs-lookup"><span data-stu-id="46d7b-193">An upgrade isn't required in order to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="46d7b-194">ดังนั้น คุณเพิ่งได้ทำตามขั้นตอนในส่วน "ดาวน์โหลดแพคเกจสามารถปรับใช้ได้ในการอัพเกรดข้อมูลล่าสุด" ของหัวข้อดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="46d7b-194">Therefore, you just have follow the steps in the "Download the latest data upgrade deployable package" section of that topic.</span></span> <span data-ttu-id="46d7b-195">คุณสามารถข้ามขั้นตอนอื่นๆ ทั้งหมดในหัวข้อได้</span><span class="sxs-lookup"><span data-stu-id="46d7b-195">You can skip all the other steps in the topic.</span></span>

#### <a name="run-scripts-against-the-finance-and-operations-database"></a><span data-ttu-id="46d7b-196">เรียกใช้สคริปต์เทียบกับฐานข้อมูล Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="46d7b-196">Run scripts against the Finance and Operations database</span></span>

<span data-ttu-id="46d7b-197">เรียกใช้สคริปต์ต่อไปนี้เทียบกับฐานข้อมูล Finance and Operations (ไม่ใช่เทียบกับฐานข้อมูลการรายงานทางการเงิน)</span><span class="sxs-lookup"><span data-stu-id="46d7b-197">Run the following scripts against the Finance and Operations database (not against the Financial reporting database):</span></span>

- <span data-ttu-id="46d7b-198">DataUpgrade.zip\\AosService\\สคริปต์\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="46d7b-198">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
- <span data-ttu-id="46d7b-199">DataUpgrade.zip\\AosService\\สคริปต์\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="46d7b-199">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="46d7b-200">สคริปต์เหล่านี้ช่วยรับรองว่าการตั้งค่าผู้ใช้ บทบาท และการติดตามการเปลี่ยนแปลง ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="46d7b-200">These scripts help guarantee that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a><span data-ttu-id="46d7b-201">เรียกใช้คำสั่ง Windows PowerShell เพื่อรีเซ็ตฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="46d7b-201">Run a Windows PowerShell command to reset the database</span></span>

<span data-ttu-id="46d7b-202">บนคอมพิวเตอร์ AOS เริ่มต้น Microsoft Windows PowerShell ให้เป็นผู้ดูแลระบบ และรันคำสั่งต่อไปนี้เพื่อรีเซ็ตการรวมระหว่าง Finance and Operations และการรายงานทางการเงิน:</span><span class="sxs-lookup"><span data-stu-id="46d7b-202">On the AOS computer, start Microsoft Windows PowerShell as an administrator, and run the following commands to reset the integration between Finance and Operations and Financial reporting.</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

<span data-ttu-id="46d7b-203">นี่เป็นคำอธิบายเกี่ยวกับพารามิเตอร์ในคำสั่ง **รีเซ็ต DatamartIntegration** :</span><span class="sxs-lookup"><span data-stu-id="46d7b-203">Here is an explanation of the parameters in the **Reset-DatamartIntegration** command:</span></span>

- <span data-ttu-id="46d7b-204">ค่าที่ถูกต้องสำหรับ **-เหตุผล** คือ **SERVICING** **BADDATA** และ **OTHER**</span><span class="sxs-lookup"><span data-stu-id="46d7b-204">The valid values for **-Reason** are **SERVICING**, **BADDATA**, and **OTHER**.</span></span>
- <span data-ttu-id="46d7b-205">พารามิเตอร์  **-ReasonDetail** เป็นข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="46d7b-205">The **-ReasonDetail** parameter is free text.</span></span>
- <span data-ttu-id="46d7b-206">เหตุผลและรายละเอียดเหตุผล จะถูกบันทึกในการตรวจสอบการตรวจวัดระยะไกล/สภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="46d7b-206">The reason and reason detail will be recorded in telemetry/environment monitoring.</span></span>

> [!NOTE]
> <span data-ttu-id="46d7b-207">หลังจากที่คุณรันคำสั่ง ระบบจะขอให้คุณป้อน **Y** เพื่อยืนยันว่า คุณต้องรีเซ็ตฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="46d7b-207">After you run the commands, you will be asked to enter **Y** to confirm that you want to reset the database.</span></span>

#### <a name="restart-services"></a><span data-ttu-id="46d7b-208">เริ่มการบริการอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="46d7b-208">Restart services</span></span>

<span data-ttu-id="46d7b-209">ใช้ services.msc เพื่อเริ่มการทำงานของบริการที่คุณหยุดการทำงานก่อนหน้านี้ใหม่:</span><span class="sxs-lookup"><span data-stu-id="46d7b-209">Use services.msc to restart the services that you stopped earlier:</span></span>

- <span data-ttu-id="46d7b-210">บริการเผยแพร่เวิลด์ไวด์เว็บ (บนคอมพิวเตอร์ AOS ทั้งหมด)</span><span class="sxs-lookup"><span data-stu-id="46d7b-210">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="46d7b-211">การจัดการชุดงานของ Microsoft Dynamics 365 for Finance and Operations (บนคอมพิวเตอร์ AOS ที่ไม่ใช่แบบส่วนตัวเท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="46d7b-211">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="46d7b-212">บริการกระบวนการ Management Reporter 2012 (บนคอมพิวเตอร์ BI เท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="46d7b-212">Management Reporter 2012 Process Service (on BI computers only)</span></span>

#### <a name="import-report-definitions"></a><span data-ttu-id="46d7b-213">นำเข้าข้อกำหนดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="46d7b-213">Import report definitions</span></span>

<span data-ttu-id="46d7b-214">นำเข้าการออกแบบรายงานของคุณจากตัวออกแบบรายงาน โดยใช้ไฟล์ที่ถูกสร้างขึ้นระหว่างการส่งออก:</span><span class="sxs-lookup"><span data-stu-id="46d7b-214">Import your report designs from Report designer by using the file that was created during the export.</span></span>

1. <span data-ttu-id="46d7b-215">ในตัวออกแบบรายงาน เลือก **บริษัท** &gt; **กลุ่มบล็อคส่วนประกอบ**</span><span class="sxs-lookup"><span data-stu-id="46d7b-215">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="46d7b-216">เลือกกลุ่มบล็อคส่วนประกอบที่จะส่งออก และจากนั้นเลือก **ส่งออก**</span><span class="sxs-lookup"><span data-stu-id="46d7b-216">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="46d7b-217">สำหรับ Finance and Operations สนับสนุนกลุ่มบล็อคส่วนประกอบเพียงหนึ่งรายการเท่านั้น **ค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="46d7b-217">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="46d7b-218">เลือกบล็อคส่วนประกอบ **เริ่มต้น** และจากนั้นเลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="46d7b-218">Select the **Default** building block, and then select **Import**.</span></span>
4. <span data-ttu-id="46d7b-219">เลือกไฟล์ที่ประกอบด้วยข้อกำหนดของรายงานที่ส่งออก แล้วจากนั้นเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="46d7b-219">Select the file that contains the exported report definitions, and then select **Open**.</span></span>
5. <span data-ttu-id="46d7b-220">ในกล่องโต้ตอบ **นำเข้า** เลือกข้อกำหนดของรายงานที่จะนำเข้า:</span><span class="sxs-lookup"><span data-stu-id="46d7b-220">In the **Import** dialog box, select the report definitions to import:</span></span>

    - <span data-ttu-id="46d7b-221">หากต้องการนำเข้าข้อกำหนดของรายงานและบล็อคส่วนประกอบที่เกี่ยวข้องทั้งหมด เลือก **เลือกทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="46d7b-221">To import all the report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="46d7b-222">หากต้องการนำเข้ารายงาน แถว คอลัมน์ ลำดับ หรือชุดมิติที่เฉพาะเจาะจง เลือกรายงาน แถว คอลัมน์ ลำดับ หรือชุดมิติที่จะนำเข้า</span><span class="sxs-lookup"><span data-stu-id="46d7b-222">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6. <span data-ttu-id="46d7b-223">เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="46d7b-223">Select **Import**.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a><span data-ttu-id="46d7b-224">รีเซ็ต data mart การรายงานทางการเงินสำหรับ Finance and Operations (on-premises)</span><span class="sxs-lookup"><span data-stu-id="46d7b-224">Reset the Financial reporting data mart for Finance and Operations (on-premises)</span></span>

1. <span data-ttu-id="46d7b-225">แนะนำให้ผู้ใช้ทั้งหมดออกจากตัวออกแบบรายงานและพื้นที่การรายงานทางการเงินของ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="46d7b-225">Instruct all users to exit Report designer and the Financial reporting area of Finance and Operations.</span></span>
2. <span data-ttu-id="46d7b-226">รันสคริปต์ต่อไปนี้โดยเทียบกับฐานข้อมูลการรายงานทางการเงิน (MRDB)</span><span class="sxs-lookup"><span data-stu-id="46d7b-226">Run the following script against the Financial reporting database (MRDB).</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. <span data-ttu-id="46d7b-227">ตัดให้สั้นลงหรือลบเรกคอร์ดทั้งหมดจากตาราง FINANCIALREPORTS ในฐานข้อมูล Finance and Operations (AXDB)</span><span class="sxs-lookup"><span data-stu-id="46d7b-227">Truncate or delete all records from the FINANCIALREPORTS table in the Finance and Operations database (AXDB).</span></span>
4. <span data-ttu-id="46d7b-228">ตัดให้สั้นลงหรือลบเรกคอร์ดทั้งหมดจากตาราง FINANCIALREPORTVERSION ถ้ามีตารางนี้อยู่ในฐานข้อมูล Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="46d7b-228">Truncate or delete all records from the FINANCIALREPORTVERSION table, if this table exists in the Finance and Operations database.</span></span> <span data-ttu-id="46d7b-229">ถ้าไม่มีตารางนี้อยู่ในฐานข้อมูล Finance and Operations ให้ข้ามขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="46d7b-229">If the table doesn't exist in the Finance and Operations database, skip this step.</span></span>
5. <span data-ttu-id="46d7b-230">รันสคริปต์ **ResetDatamart.sql** โดยเทียบกับฐานข้อมูลการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="46d7b-230">Run the **ResetDatamart.sql** script against the Financial reporting database.</span></span> <span data-ttu-id="46d7b-231">สคริปต์นี้ปิดใช้งานการรวม data mart ลบข้อมูล data mart ทั้งหมด และเปิดใช้งานการรวม data mart อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="46d7b-231">This script disables the data mart integration, deletes all the data mart data, and then reenables the data mart integration.</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. <span data-ttu-id="46d7b-232">หลังจากการรีเซ็ต คุณสามารถตรวจสอบการรีโหลดข้อมูลด้วยตนเองได้ โดยการรันการสอบถามต่อไปนี้เทียบกับฐานข้อมูลการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="46d7b-232">After the reset, you can manually verify the data reload by running the following query against the Financial reporting database.</span></span>

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    <span data-ttu-id="46d7b-233">ยืนยันว่า แถวทั้งหมดมีค่า **LastRunTime** และ **StateType** ถูกตั้งค่าเป็น **5**</span><span class="sxs-lookup"><span data-stu-id="46d7b-233">Confirm that all rows have a **LastRunTime** value, and that **StateType** is set to **5**.</span></span> <span data-ttu-id="46d7b-234">ค่า **StateType** เท่ากับ **5** บ่งชี้ว่า ข้อมูลถูกรีโหลดเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="46d7b-234">A **StateType** value of **5** indicates that the data was successfully reloaded.</span></span> <span data-ttu-id="46d7b-235">ค่าเท่ากับ **7** บ่งชี้สถานะที่มีข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="46d7b-235">A value of **7** indicates a faulted state.</span></span> <span data-ttu-id="46d7b-236">บางครั้ง แผนผังลำดับชั้นขององค์กรมีสถานะนี้ในครั้งแรกที่รัน</span><span class="sxs-lookup"><span data-stu-id="46d7b-236">Sometimes, the Organization Hierarchy map has this state the first time that it runs.</span></span> <span data-ttu-id="46d7b-237">อย่างไรก็ตาม สถานะที่มีข้อบกพร่อง แต่ควรได้รับการแก้ไขโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="46d7b-237">However, the faulted state but should be automatically resolved.</span></span>

