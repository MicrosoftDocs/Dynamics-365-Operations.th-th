---
title: โฮมเพจข้อมูลเชิงลึกทางการเงิน (ตัวอย่าง)
description: ข้อมูลเชิงลึกของการเงินจะให้แบบจำลองที่สามารถจัดโครงแบบได้และมีการขยายตัวเพื่อช่วยให้คุณสามารถคาดการณ์กระแสเงินสดของบริษัทของคุณได้อย่างถูกต้อง คาดการณ์เมื่อคุณจะได้รับการชำระเงินสำหรับลูกหนี้ที่ค้างชำระ และสร้างข้อเสนองบประมาณที่สามารถเพิ่มความเร็วในการจัดทำงบ ลักษณะการทำงานทั้งหมดเหล่านี้จะขึ้นอยู่กับแบบจำลองการเรียนรู้ของเครื่องอัจฉริยะ
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4876d2d4ad79dc09ce4b372eedf4c6ab31930957
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222521"
---
# <a name="finance-insights-home-page-preview"></a><span data-ttu-id="9bd32-104">โฮมเพจข้อมูลเชิงลึกทางการเงิน (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="9bd32-104">Finance insights home page (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="9bd32-105">ข้อมูลเชิงลึกของการเงินจะให้แบบจำลองที่สามารถจัดโครงแบบได้และมีการขยายตัวเพื่อช่วยให้คุณสามารถคาดการณ์กระแสเงินสดของบริษัทของคุณได้อย่างถูกต้อง คาดการณ์เมื่อคุณจะได้รับการชำระเงินสำหรับลูกหนี้ที่ค้างชำระ และสร้างข้อเสนองบประมาณที่สามารถเพิ่มความเร็วในการจัดทำงบ</span><span class="sxs-lookup"><span data-stu-id="9bd32-105">Finance insights provides configurable and extensible models to help you accurately and intelligently predict your company's cash flow, predict when you will receive payment for outstanding receivables, and generate a budget proposal that can speed up your budgeting process.</span></span> <span data-ttu-id="9bd32-106">ลักษณะการทำงานทั้งหมดเหล่านี้จะขึ้นอยู่กับแบบจำลองการเรียนรู้ของเครื่องอัจฉริยะ</span><span class="sxs-lookup"><span data-stu-id="9bd32-106">All these features are based on intelligent machine learning models.</span></span> <span data-ttu-id="9bd32-107">เมื่อมีการรวมความสามารถใหม่ ๆ เข้ากับระบบอัตโนมัติในการชำระเงินของผู้จัดจำหน่ายและการเรียกเก็บเงิน จะมีระบบการเงินที่สมบูรณ์และฉลาดซึ่งผลักดันการตัดสินใจ และช่วยให้คุณสามารถดำเนินการเพื่อตอบสนองต่อความท้าทายทางธุรกิจในปัจจุบันและที่คาดการณ์ไว้ได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="9bd32-107">When these new capabilities are combined with automation in vendor payments and collections, they provide a rich and intelligent financial system that drives decision making and helps you take action to respond effectively to current and anticipated business challenges.</span></span>

<span data-ttu-id="9bd32-108">ตัวอย่างข้อมูลเชิงลึกของการเงินจะพร้อมใช้งานสำหรับการใช้งานทดลองในสหรัฐอเมริกา ยุโรป และสหราชอาณาจักร</span><span class="sxs-lookup"><span data-stu-id="9bd32-108">Finance insights preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="9bd32-109">Microsoft กำลังเพิ่มการสนับสนุนสำหรับภูมิภาคเพิ่มเติมมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="9bd32-109">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="9bd32-110">คุณลักษณะตัวอย่างควรเปิดใช้งานเฉพาะในสภาพแวดล้อมที่มี Sandbox ระดับ 2 เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9bd32-110">Preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="9bd32-111">การตั้งค่าและโมเดลปัญญาประดิษฐ์ (AI) ที่สร้างขึ้นในสภาพแวดล้อม Sandbox ไม่สามารถถูกย้ายไปยังสภาพแวดล้อมการผลิต</span><span class="sxs-lookup"><span data-stu-id="9bd32-111">Setup and artificial intelligence (AI) models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="9bd32-112">สำหรับข้อมูลเพิ่มเติม ให้ดู [เงื่อนไขการใช้เพิ่มเติมสำหรับการแสดงตัวอย่าง Microsoft Dynamics 365](/dynamics365/legal/supp-dynamics365-preview#:~:text=Supplemental%20Terms%20of%20Use%20for%20Microsoft%20Dynamics%20365,%28governing%20your%20use%20of%20Microsoft%20Dynamics%20365%20Online%29.)</span><span class="sxs-lookup"><span data-stu-id="9bd32-112">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](/dynamics365/legal/supp-dynamics365-preview#:~:text=Supplemental%20Terms%20of%20Use%20for%20Microsoft%20Dynamics%20365,%28governing%20your%20use%20of%20Microsoft%20Dynamics%20365%20Online%29.).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9bd32-113">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="9bd32-113">Prerequisites</span></span>

<span data-ttu-id="9bd32-114">ส่วนนี้แสดงรายการความต้องการสำหรับการใช้ข้อมูลเชิงลึกทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="9bd32-114">This section lists the requirements for using Finance insights.</span></span> <span data-ttu-id="9bd32-115">สามารถเชื่อมโยงไปยังแหล่งที่มาของข้อมูลเพิ่มเติมได้ทุกเมื่อ</span><span class="sxs-lookup"><span data-stu-id="9bd32-115">Wherever possible, links to sources of additional information are provided.</span></span>

### <a name="legal-requirements"></a><span data-ttu-id="9bd32-116">ข้อกำหนดทางกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="9bd32-116">Legal requirements</span></span>

<span data-ttu-id="9bd32-117">เมื่อต้องการใช้สำหรับโปรแกรมแสดงตัวอย่าง ให้กรอก [ตัวอย่างข้อมูลเชิงลึกของการเงินสำหรับข้อตกลง Dynamics 365 Finance](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u)</span><span class="sxs-lookup"><span data-stu-id="9bd32-117">To apply for the preview program, fill out the [Finance insights Preview for Dynamics 365 Finance agreement](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u).</span></span>

### <a name="system-requirements"></a><span data-ttu-id="9bd32-118">ความต้องการของระบบ</span><span class="sxs-lookup"><span data-stu-id="9bd32-118">System requirements</span></span>

<span data-ttu-id="9bd32-119">ต้องมีสภาพแวดล้อมของ Sandbox ระดับ 2 (หลายกล่อง) เพื่อแสดงตัวอย่างข้อมูลเชิงลึกของการเงิน</span><span class="sxs-lookup"><span data-stu-id="9bd32-119">A Tier-2 sandbox environment (multi-box) is required to preview Finance insights.</span></span> <span data-ttu-id="9bd32-120">สำหรับข้อมูลประวัติความเป็นมาเกี่ยวกับสภาพแวดล้อม ดูที่ [การวางแผนสภาพแวดล้อม](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)</span><span class="sxs-lookup"><span data-stu-id="9bd32-120">For background information about environments, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>

### <a name="version-requirements"></a><span data-ttu-id="9bd32-121">ข้อกำหนดรุ่น</span><span class="sxs-lookup"><span data-stu-id="9bd32-121">Version requirements</span></span>

<span data-ttu-id="9bd32-122">เอกสารนี้ใช้กับรุ่น 10.0.11 ของแอป Finance and Operations (แพลตฟอร์มอัพเดต 35) และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="9bd32-122">This document applies to version 10.0.11 of Finance and Operations apps (Platform update 35), and later versions.</span></span>

### <a name="historical-data-requirements"></a><span data-ttu-id="9bd32-123">ข้อกำหนดเกี่ยวกับข้อมูลในอดีต</span><span class="sxs-lookup"><span data-stu-id="9bd32-123">Historical data requirements</span></span>

<span data-ttu-id="9bd32-124">จำเป็นต้องมีมูลค่าของใบแจ้งหนี้ของลูกค้าอย่างน้อยหนึ่งปีเพื่อฝึกแบบจำลองการเรียนรู้ของเครื่องที่ใช้สำหรับลักษณะการทำงานการคาดการณ์การชำระเงินของลูกค้าได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="9bd32-124">At least one year's worth of customer invoices is required to correctly train the machine learning model that is used for the Customer payment predictions feature.</span></span>

<span data-ttu-id="9bd32-125">ข้อมูลตัวอย่างจะพร้อมใช้งานสำหรับระบบการสาธิตที่มีชุดข้อมูลสาธิต Contoso</span><span class="sxs-lookup"><span data-stu-id="9bd32-125">Sample data is available for demo systems that have the Contoso demo data set.</span></span>

### <a name="role-and-permission-requirements"></a><span data-ttu-id="9bd32-126">ข้อกำหนดของบทบาทและสิทธิ์การได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="9bd32-126">Role and permission requirements</span></span>

<span data-ttu-id="9bd32-127">การเปลี่ยนแปลงจะทำกับ Microsoft Dynamics 365 Finance, Microsoft Dynamics Lifecycle Services (LCS), Microsoft, Power Apps และ Azure</span><span class="sxs-lookup"><span data-stu-id="9bd32-127">Changes will be made to Microsoft Dynamics 365 Finance, Microsoft Dynamics Lifecycle Services (LCS), Power Apps, and Azure.</span></span> <span data-ttu-id="9bd32-128">จำเป็นต้องมีสิทธิ์ที่ถูกต้องในสภาพแวดล้อมเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="9bd32-128">Correct permissions are required across these environments.</span></span> <span data-ttu-id="9bd32-129">นี่คือตัวอย่างบางตัวอย่างที่จะเปลี่ยนแปลง:</span><span class="sxs-lookup"><span data-stu-id="9bd32-129">Here are some examples of the changes that will be made:</span></span>

- <span data-ttu-id="9bd32-130">สภาพแวดล้อมใหม่จะถูกสร้างขึ้นใน Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="9bd32-130">A new environment will be created in Microsoft Power Platform.</span></span>
- <span data-ttu-id="9bd32-131">บัญชีพื้นที่จัดเก็บ Key Vault และโปรแกรมประยุกต์จะถูกสร้างขึ้นใน Azure</span><span class="sxs-lookup"><span data-stu-id="9bd32-131">A storage account, key vault, and application will be created in Azure.</span></span>
- <span data-ttu-id="9bd32-132">ผู้ดูแลระบบผู้เช่าไดเรกทอรีที่ใช้งานอยู่จะต้องได้รับอนุญาตให้โปรแกรมประยุกต์ AI Builder เข้าถึงที่จัดเก็บข้อมูลดิบ</span><span class="sxs-lookup"><span data-stu-id="9bd32-132">The Active Directory tenant administrator will have to authorize the AI Builder application to access the data lake.</span></span>
- <span data-ttu-id="9bd32-133">ลักษณะการทำงานนี้จะเปิดอยู่ใน Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="9bd32-133">The feature will be turned on in Dynamics 365.</span></span>

<span data-ttu-id="9bd32-134">ความคุ้นเคยกับกระบวนการในการสร้างและการจัดการทรัพยากรใน Azure, Microsoft Dataverse และ LCS จะมีประโยชน์เมื่อคุณดำเนินการนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="9bd32-134">Familiarity with the process of creating and managing resources in Azure, Microsoft Dataverse, and LCS will be helpful as you complete this process.</span></span>

## <a name="configure-finance-insights"></a><span data-ttu-id="9bd32-135">ตั้งค่าคอนฟิกข้อมูลเชิงลึกของการเงิน</span><span class="sxs-lookup"><span data-stu-id="9bd32-135">Configure Finance insights</span></span>

<span data-ttu-id="9bd32-136">คุณต้องทำขั้นตอนการตั้งค่าคอนฟิกบางอย่างให้เสร็จสมบูรณ์ก่อนจึงจะสามารถใช้ข้อมูลเชิงลึกทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="9bd32-136">You must complete some configuration steps before you can use Finance insights.</span></span> <span data-ttu-id="9bd32-137">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่า Finance Insights นี้ ดูที่</span><span class="sxs-lookup"><span data-stu-id="9bd32-137">For more information about how to configure Finance insights, see:</span></span>
  - <span data-ttu-id="9bd32-138">สำหรับรุ่นไม่เกิน 10.0.19: [การตั้งค่าคอนฟิกสำหรับ Finance insights - ไม่เกินรุ่น 10.0.19](configure-for-fin-insites.md)</span><span class="sxs-lookup"><span data-stu-id="9bd32-138">For versions up to 10.0.19: [Configuration for Finance insights - versions up to 10.0.19](configure-for-fin-insites.md).</span></span>
  - <span data-ttu-id="9bd32-139">สำหรับรุ่น 10.0.20 และอื่นๆ: [การตั้งค่าคอนฟิกสำหรับ Finance Insights (ตัวอย่าง) - รุ่น 10.0.20 และอื่นๆ](configure-for-fin-insites-PubPrvw.md)</span><span class="sxs-lookup"><span data-stu-id="9bd32-139">For versions 10.0.20 and beyond: [Configuration for Finance Insights (preview) - versions 10.0.20 and beyond](configure-for-fin-insites-PubPrvw.md).</span></span>

## <a name="create-a-data-integrator-project"></a><span data-ttu-id="9bd32-140">สร้างโครงการตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9bd32-140">Create a data integrator project</span></span>

<span data-ttu-id="9bd32-141">คุณจะต้องสร้างโครงการตัวรวมข้อมูลเพื่อให้ข้อมูลที่แบบจำลองการเรียนรู้ของเครื่องสร้างขึ้นสามารถไหลเข้า Dynamics 365 Finance ได้</span><span class="sxs-lookup"><span data-stu-id="9bd32-141">You'll need to create a data integrator project so that data that the machine learning model generates can flow into Dynamics 365 Finance.</span></span> <span data-ttu-id="9bd32-142">สำหรับขั้นตอนในการสร้างโครงการนั้น ให้ดูที่ [สร้างโครงการตัวรวมข้อมูล](create-data-integrate-project.md)</span><span class="sxs-lookup"><span data-stu-id="9bd32-142">For the steps to create that project, see [Create a data integrator project](create-data-integrate-project.md).</span></span>

## <a name="enable-finance-insights-capabilities"></a><span data-ttu-id="9bd32-143">เปิดใช้งานความสามารถเชิงลึกของการเงิน</span><span class="sxs-lookup"><span data-stu-id="9bd32-143">Enable Finance insights capabilities</span></span>

<span data-ttu-id="9bd32-144">เมื่อคุณดำเนินการขั้นตอนการตั้งค่าคอนฟิกเสร็จเรียบร้อยแล้วและตั้งค่าข้อมูลสาธิตแล้วคุณต้องเปิดและตั้งค่าความสามารถแต่ละรายการที่คุณวางแผนที่จะใช้: การคาดการณ์การชำระเงินของลูกค้า การคาดการณ์กระแสเงินสด และข้อเสนองบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9bd32-144">When you've completed the configuration steps and set up demo data, you must turn on and set up each capability that you plan to use: customer payment predictions, cash flow forecasting, and budget proposals.</span></span>

### <a name="enable-customer-payment-predictions"></a><span data-ttu-id="9bd32-145">เปิดใช้งานการคาดคะเนการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9bd32-145">Enable Customer payment predictions</span></span>
<span data-ttu-id="9bd32-146">ถ้าคุณกำลังใช้ข้อมูลสาธิตในการทดสอบการคาดการณ์การชำระเงินของลูกค้า คุณอาจต้องนำเข้าข้อมูลการสาธิตเพิ่มเติมเพื่อสร้างแบบจำลอง AI ของคุณเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="9bd32-146">If you are using demo data to test customer payment predictions, you may have to import additional demo data to create your AI model successfully.</span></span> 

<span data-ttu-id="9bd32-147">เมื่อต้องการเปิดใช้งานการคาดคะเนการชำระเงินของลูกค้า คุณต้องทำการตั้งค่าขั้นตอนเพื่อสร้างแบบจำลองการเรียนรู้ของเครื่องที่ใช้ข้อมูลขององค์กรของคุณในการสร้างการคาดการณ์เมื่อลูกค้ามีแนวโน้มที่จะชำระใบแจ้งหนี้ที่ค้างชำระ และเมื่อมีการชำระเงินตามใบแจ้งหนี้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="9bd32-147">To enable Customer payment predictions, you must complete a set of steps to build a machine learning model that uses your organization's data your organization's data to generate predictions about when customers are likely to pay outstanding invoices, and when specific invoices are likely to be paid.</span></span> <span data-ttu-id="9bd32-148">สำหรับข้อมูลเพิ่มเติมและขั้นตอนเฉพาะในการทำให้เสร็จสมบูรณ์ ให้ดูที่ [เปิดใช้งานการคาดการณ์การชำระเงินของลูกค้า](enable-cust-paymnt-prediction.md)</span><span class="sxs-lookup"><span data-stu-id="9bd32-148">For more information and the specific steps to complete, see [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span> 

### <a name="enable-cash-flow-forecasting"></a><span data-ttu-id="9bd32-149">เปิดใช้งานการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="9bd32-149">Enable Cash flow forecasting</span></span>
<span data-ttu-id="9bd32-150">เมื่อต้องการเปิดใช้งานการคาดการณ์กระแสเงินสด คุณต้องทำการตั้งค่าขั้นตอนนี้ให้เสร็จสมบูรณ์เพื่อสร้างแบบจำลองการเรียนรู้ของเครื่องที่ใช้ข้อมูลขององค์กรของคุณในการสร้างการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="9bd32-150">To enable Cash flow forecasting, you must complete a set of steps to build a machine learning model that uses your organization's data to generate cash flow forecasts.</span></span> <span data-ttu-id="9bd32-151">สำหรับข้อมูลเพิ่มเติมและขั้นตอนเฉพาะในการทำให้เสร็จสมบูรณ์ ให้ดูที่ [เปิดใช้งานการคาดการณ์กระแสเงินสด](enable-cash-flow-forecasting.md)</span><span class="sxs-lookup"><span data-stu-id="9bd32-151">For more information and the specific steps to complete, see [Enable cash flow forecasting](enable-cash-flow-forecasting.md).</span></span>

### <a name="enable-budget-proposals"></a><span data-ttu-id="9bd32-152">เปิดใช้งานข้อเสนองบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9bd32-152">Enable budget proposals</span></span>

<span data-ttu-id="9bd32-153">ลักษณะการทำงานของข้อเสนองบประมาณใช้แบบจำลองการเรียนรู้ของเครื่องพร้อมกับข้อมูลในอดีตขององค์กรของคุณเพื่อสร้างข้อเสนองบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9bd32-153">The Budget proposals feature uses a machine learning model along with your organization's historical data to generate a budget proposal.</span></span> <span data-ttu-id="9bd32-154">ข้อเสนอที่สร้างขึ้นสามารถช่วยคุณเริ่มต้นกระบวนการจัดทำงบประมาณที่มีประสิทธิภาพมากขึ้นและมีประสิทธิภาพกว่ากระบวนการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9bd32-154">The generated proposal can help you begin a budgeting process that is more effective and efficient than a manual process.</span></span> <span data-ttu-id="9bd32-155">สำหรับขั้นตอนเฉพาะเพื่อเปิดใช้งานลักษณะการทำงานนี้ ให้ดูที่ [เปิดใช้งานข้อเสนองบประมาณ](enable-budget-proposal.md)</span><span class="sxs-lookup"><span data-stu-id="9bd32-155">For the specific steps to enable this feature, see  [Enable budget proposals](enable-budget-proposal.md).</span></span> 

## <a name="using-finance-insights-features"></a><span data-ttu-id="9bd32-156">การใช้คุณสมบัติเชิงลึกของการเงิน</span><span class="sxs-lookup"><span data-stu-id="9bd32-156">Using Finance insights features</span></span>

### <a name="using-customer-payment-predictions"></a><span data-ttu-id="9bd32-157">การใช้การคาดการณ์การชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9bd32-157">Using Customer payment predictions</span></span>

<span data-ttu-id="9bd32-158">การคาดการณ์กระแสเงินสดอัจฉริยะสร้างขึ้นบนฟังก์ชันการคาดการณ์กระแสเงินสดที่มีอยู่ใน Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="9bd32-158">The intelligent cash flow forecasting is built on top of existing the cash flow forecasting functionality in Dynamics 365 Finance.</span></span> <span data-ttu-id="9bd32-159">เมื่อต้องการตรวจทานความสามารถที่มีอยู่ ให้ดูที่ [การคาดการณ์กระแสเงินสด](../cash-bank-management/cash-flow-forecasting.md)</span><span class="sxs-lookup"><span data-stu-id="9bd32-159">To review the existing capability, see [Cash flow forecasting](../cash-bank-management/cash-flow-forecasting.md).</span></span>

- <span data-ttu-id="9bd32-160">หากต้องการทราบวิธีการคาดคะเนการชำระเงินของลูกค้าสามารถให้ข้อมูลที่จำเป็นในการจัดการกิจกรรมการเรียกเก็บเงิน ให้ดูที่ [ใช้การคาดการณ์การชำระเงินของลูกค้า](use-customer-payment-predictions.md)</span><span class="sxs-lookup"><span data-stu-id="9bd32-160">To learn how Customer payment predictions can provide the information needed to proactively being collection activities, see [Use Customer payment predictions](use-customer-payment-predictions.md).</span></span>
- <span data-ttu-id="9bd32-161">สำหรับข้อมูลที่สามารถช่วยคุณในการประเมินประสิทธิภาพของแบบจำลองการคาดการณ์หลังจากที่คุณเริ่มใช้งานลักษณะการทำงานแล้ว ให้ดูที่ [การประเมินแบบจำลองการคาดการณ์การชำระเงินของลูกค้าเริ่มต้น](evaluate-payment-prediction.md)</span><span class="sxs-lookup"><span data-stu-id="9bd32-161">For information that can help you evaluate the effectiveness of the prediction model after you've started using the feature, see [Evaluate the initial customer payment prediction model](evaluate-payment-prediction.md).</span></span>
- <span data-ttu-id="9bd32-162">สำหรับข้อมูลที่สามารถช่วยคุณปรับปรุงข้อมูลที่ใช้ในการสร้างการคาดการณ์จึงทำให้มีประสิทธิภาพมากขึ้น ให้ดูที่ [การปรับปรุงแบบจำลองการคาดการณ์](improve-model.md)</span><span class="sxs-lookup"><span data-stu-id="9bd32-162">For information that can help you adjust the data that is used to build the prediction and thereby improve its effectiveness, see [Improve the prediction model](improve-model.md).</span></span>

<span data-ttu-id="9bd32-163">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับผลลัพธ์ของแบบจำลองการคาดคะเน AI โปรดดูที่ [ผลลัพธ์ของแบบจำลองการเรียนรู้ของเครื่อง](confusion-matrix.md)</span><span class="sxs-lookup"><span data-stu-id="9bd32-163">To learn more about the results of AI prediction models, see [Results of machine learning models](confusion-matrix.md).</span></span>

### <a name="using-cash-flow-forecasts"></a><span data-ttu-id="9bd32-164">การใช้การคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="9bd32-164">Using Cash flow forecasts</span></span>

<span data-ttu-id="9bd32-165">ความสามารถในการคาดการณ์กระแสเงินสดช่วยให้คุณสามารถประเมินตำแหน่งเงินสดของคุณได้อย่างถูกต้องมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="9bd32-165">The Cash flow forecast capability can help you more accurately estimate your cash position.</span></span> 

- <span data-ttu-id="9bd32-166">เมื่อต้องการเรียนรู้เกี่ยวกับความสามารถใหม่ในการคาดการณ์กระแสเงินสด ให้ดูที่ [การคาดการณ์กระแสเงินสด](cash-flow-forecast-intro.md)</span><span class="sxs-lookup"><span data-stu-id="9bd32-166">To learn about the new capabilities in Cash flow forecasts see [Cash flow forecast](cash-flow-forecast-intro.md).</span></span>
- <span data-ttu-id="9bd32-167">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการนำเข้าข้อมูลภายนอกที่จะรวมไว้ในการคาดการณ์กระแสเงินสดของคุณที่นี่ ให้ดูที่ [ใช้ข้อมูลภายนอกในการคาดการณ์กระแสเงินสด](external-data-in-cash-flow.md)</span><span class="sxs-lookup"><span data-stu-id="9bd32-167">For information about importing external data to include in your cashflow forecast here, see [Use external data in cash flow forecasts](external-data-in-cash-flow.md).</span></span> 
- <span data-ttu-id="9bd32-168">สำหรับข้อมูลเกี่ยวกับวิธีการใช้แบบจำลอง AI กับโครงการกระแสเงินสดระยะสั้น โปรดดูที่ [ฐานะเงินสด](cash-position.md)</span><span class="sxs-lookup"><span data-stu-id="9bd32-168">For information about how to use an AI model to project near term cash flow, see [Cash position](cash-position.md).</span></span>
- <span data-ttu-id="9bd32-169">สำหรับข้อมูลเกี่ยวกับการบันทึกตำแหน่งของกระแสเงินสดและการคาดการณ์กระแสเงินสดเป็นสแนปช็อต และเพื่อเปรียบเทียบสแนปช็อตเป็นจริง โปรดดู [ภาพรวมของสแนปช็อต](payment-snapshots.md)</span><span class="sxs-lookup"><span data-stu-id="9bd32-169">For information about saving cash flow positions and cash flow forecasts as snapshots, and to compare a snapshot to actuals, see [Snapshots overview](payment-snapshots.md).</span></span>

### <a name="using-budget-proposal"></a><span data-ttu-id="9bd32-170">การใช้ข้อเสนองบประมาณ</span><span class="sxs-lookup"><span data-stu-id="9bd32-170">Using Budget proposal</span></span>

<span data-ttu-id="9bd32-171">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเร่งการสร้างงบประมาณ ให้ดูที่ [ข้อเสนองบประมาณ](budget-proposals.md)</span><span class="sxs-lookup"><span data-stu-id="9bd32-171">For information about accelerating the creation of a budget, see [Budget proposals](budget-proposals.md).</span></span> 

## <a name="feedback-and-support"></a><span data-ttu-id="9bd32-172">ผลป้อนกลับและการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="9bd32-172">Feedback and support</span></span>

<span data-ttu-id="9bd32-173">โปรดส่งอีเมล์ถึง [ข้อมูลเชิงลึกของการชำระเงินของลูกค้า (ตัวอย่าง)](mailto:fiap@microsoft.com) หากคุณมีความสนใจในการให้ผลป้อนกลับหรือต้องการความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="9bd32-173">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
