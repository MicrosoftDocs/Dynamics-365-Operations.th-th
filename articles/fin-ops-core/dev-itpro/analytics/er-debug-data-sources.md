---
title: ดีบักแหล่งข้อมูลของรูปแบบ ER ที่ดําเนินการ เพื่อวิเคราะห์การแปลงและลำดับของข้อมูล
description: หัวข้อนี้อธิบายวิธีที่คุณสามารถดีบักแหล่งข้อมูลของรูปแบบ ER ที่ดําเนินการ เพื่อให้เข้าใจการแปลงและลำดับของข้อมูลที่กําหนดค่าดีขึ้น
author: NickSelin
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 3a486800f37dda7829aeeaa56a30285a92a61b9d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680793"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a><span data-ttu-id="6e016-103">ดีบักแหล่งข้อมูลของรูปแบบ ER ที่ดําเนินการ เพื่อวิเคราะห์การแปลงและลำดับของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6e016-103">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="6e016-104">เมื่อคุณ [ตั้งค่าคอนฟิก](tasks/er-format-configuration-2016-11.md) การรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารขาออก คุณกำหนดวิธีการที่จะใช้ในการดึงข้อมูลจากใบสมัคร และป้อนข้อมูลในผลลัพธ์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="6e016-104">When you [configure](tasks/er-format-configuration-2016-11.md) an Electronic reporting (ER) solution to generate outbound documents, you define the methods that are used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="6e016-105">เมื่อต้องการให้การสนับสนุนวงจรการใช้งานของโซลูชัน ER มีประสิทธิภาพมากขึ้น โซลูชันของคุณควรประกอบด้วย [แบบจําลองข้อมูล](general-electronic-reporting.md#DataModelComponent) ER และส่วนประกอบ [การแม็ป](general-electronic-reporting.md#ModelMappingComponent) และส่วนประกอบการแม็ป [รูปแบบ](general-electronic-reporting.md#FormatComponentOutbound) ER เพื่อให้การแม็ปแบบจำลองเป็นแบบเฉพาะใบสมัคร ในขณะที่ส่วนประกอบอื่นๆ ยังคงไม่ระบุใบสมัครเหมือนเดิม</span><span class="sxs-lookup"><span data-stu-id="6e016-105">To make the life cycle support of the ER solution more efficient, your solution should consist of an ER [data model](general-electronic-reporting.md#DataModelComponent) and its [mapping](general-electronic-reporting.md#ModelMappingComponent) components, and also an ER [format](general-electronic-reporting.md#FormatComponentOutbound) and its mapping components, so that the model mapping is application-specific, whereas other components remain application-agnostic.</span></span> <span data-ttu-id="6e016-106">ดังนั้น ส่วนประกอบ ER หลายตัวอาจ [ส่งผลต่อ](general-electronic-reporting.md#FormatComponentOutbound) กระบวนการป้อนข้อมูลในผลลัพธ์ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="6e016-106">Therefore, several ER components might [affect](general-electronic-reporting.md#FormatComponentOutbound) the process of entering data in the generated output.</span></span>

<span data-ttu-id="6e016-107">บางครั้ง ข้อมูลของผลลัพธ์ที่สร้างขึ้นมีลักษณะแตกต่างจากข้อมูลเดียวกันในฐานข้อมูลใบสมัคร</span><span class="sxs-lookup"><span data-stu-id="6e016-107">Sometimes, the data of the generated output looks different than the same data in the application database.</span></span> <span data-ttu-id="6e016-108">ในกรณีเหล่านี้ คุณจะต้องกําหนดว่าส่วนประกอบ ER ใดที่รับผิดชอบการแปลงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6e016-108">In these cases, you will want to determine which ER component is responsible for the data transformation.</span></span> <span data-ttu-id="6e016-109">คุณลักษณะดีบักเกอร์แหล่งข้อมูล ER ช่วยลดเวลาและต้นทุนที่เกี่ยวข้องกับการตรวจสอบนี้อย่างมาก</span><span class="sxs-lookup"><span data-stu-id="6e016-109">The ER data source debugger feature significantly reduces the time and cost that are involved in this investigation.</span></span> <span data-ttu-id="6e016-110">คุณสามารถยุติการดําเนินการของรูปแบบ ER และเปิดอินเทอร์เฟสดีบักเกอร์แหล่งข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="6e016-110">You can interrupt the execution of an ER format and open the data source debugger interface.</span></span> <span data-ttu-id="6e016-111">คุณสามารถเรียกดูแหล่งข้อมูลที่มีอยู่ และเลือกแหล่งข้อมูลแต่ละแหล่งสําหรับการดําเนินการ</span><span class="sxs-lookup"><span data-stu-id="6e016-111">There, you can browse the available data sources and select an individual data source for execution.</span></span> <span data-ttu-id="6e016-112">การดําเนินการด้วยตนเองนี้จําลองการดําเนินการของแหล่งข้อมูลในระหว่างการรันจริงของรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="6e016-112">This manual execution simulates the execution of the data source during the real run of an ER format.</span></span> <span data-ttu-id="6e016-113">ผลลัพธ์จะแสดงบนหน้าที่คุณสามารถวิเคราะห์ข้อมูลที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="6e016-113">The result is presented on a page where you can analyze the data that is received.</span></span>

<span data-ttu-id="6e016-114">เมื่อต้องการเปิดคุณลักษณะการดีบักแหล่งข้อมูล ให้ตั้งค่าตัวเลือก **เปิดใช้งานการดีบักข้อมูลเมื่อเรียกใช้รูปแบบ** เป็น **ใช่** ในพารามิเตอร์ผู้ใช้ ER</span><span class="sxs-lookup"><span data-stu-id="6e016-114">To turn on the data source debugging feature, set the **Enable data debugging at format run** option to **Yes** in the ER user parameters.</span></span> <span data-ttu-id="6e016-115">จากนั้น คุณสามารถเริ่มต้นการดีบักแหล่งข้อมูล ในขณะที่คุณเรียกใช้รูปแบบ ER เพื่อสร้างเอกสารขาออก</span><span class="sxs-lookup"><span data-stu-id="6e016-115">You can then start data source debugging while you run an ER format to generate outbound documents.</span></span> <span data-ttu-id="6e016-116">คุณยังสามารถใช้ตัวเลือก **เริ่มต้นการดีบัก** เพื่อเริ่มต้นการดีบักแหล่งข้อมูลสําหรับรูปแบบ ER ที่มีการตั้งค่าคอนฟิกไว้ใน [โปรแกรมออกแบบการดําเนินการ ER](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document)</span><span class="sxs-lookup"><span data-stu-id="6e016-116">You can also use the **Start debugging** option to initiate data source debugging for an ER format that is configured in the [ER Operation designer](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span></span>

<span data-ttu-id="6e016-117">หัวข้อนี้แสดงแนวทางสําหรับการเริ่มการดีบักแหล่งข้อมูลสําหรับรูปแบบ ER ที่ดําเนินการ</span><span class="sxs-lookup"><span data-stu-id="6e016-117">This topic provides guidelines for initiating data source debugging for executed ER formats.</span></span> <span data-ttu-id="6e016-118">โดยอธิบายถึงวิธีที่ข้อมูลสามารถช่วยให้คุณเข้าใจและลำดับข้อมูลและการแปลงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6e016-118">It explains how the information can help you understand the data flow and data transformations.</span></span> <span data-ttu-id="6e016-119">ตัวอย่างในหัวข้อนี้ใช้กระบวนการทางธุรกิจสําหรับการประมวลผลการชําระเงินให้แก่ผู้จัดจําหน่าย</span><span class="sxs-lookup"><span data-stu-id="6e016-119">The examples in this topic use the business process for vendor payments processing.</span></span>

## <a name="limitations"></a><span data-ttu-id="6e016-120">การจำกัด</span><span class="sxs-lookup"><span data-stu-id="6e016-120">Limitations</span></span>

<span data-ttu-id="6e016-121">ดีบักเกอร์แหล่งข้อมูลสามารถใช้เพื่อเข้าถึงข้อมูลของแหล่งข้อมูลที่ใช้ในรูปแบบ ER ที่เรียกใช้เพื่อสร้างเอกสารขาออก</span><span class="sxs-lookup"><span data-stu-id="6e016-121">The data source debugger can be used to access the data of data sources that are used in ER formats that are run to generate outbound documents.</span></span> <span data-ttu-id="6e016-122">ไม่สามารถใช้เพื่อดีบักแหล่งข้อมูลของรูปแบบ ER ที่ออกแบบมาเพื่อวิเคราะห์เอกสารขาเข้า</span><span class="sxs-lookup"><span data-stu-id="6e016-122">It can't be used to debug data sources of ER formats that are designed to parse inbound documents.</span></span>

<span data-ttu-id="6e016-123">การตั้งค่ารูปแบบ ER ต่อไปนี้ไม่สามารถเข้าถึงได้ในปัจจุบันสําหรับการดีบักแหล่งข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="6e016-123">The following settings of ER formats aren't currently accessible for data source debugging:</span></span>

- <span data-ttu-id="6e016-124">การแปลงรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="6e016-124">Format transformations</span></span>
- <span data-ttu-id="6e016-125">กฎการตรวจสอบความถูกต้องของรูปแบบและการแม็ป</span><span class="sxs-lookup"><span data-stu-id="6e016-125">Format and mapping validation rules</span></span>
- <span data-ttu-id="6e016-126">การเปิดใช้งานนิพจน์</span><span class="sxs-lookup"><span data-stu-id="6e016-126">Enabling expressions</span></span>
- <span data-ttu-id="6e016-127">รายละเอียดของการรวบรวมข้อมูลในหน่วยความจํา</span><span class="sxs-lookup"><span data-stu-id="6e016-127">Details of in-memory data collection</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6e016-128">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="6e016-128">Prerequisites</span></span>

- <span data-ttu-id="6e016-129">เมื่อต้องการดำเนินการตัวอย่างในหัวข้อนี้ให้เสร็จสมบูรณ์ คุณต้องเข้าถึงหนึ่งใน [บทบาท](../sysadmin/tasks/assign-users-security-roles.md) ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6e016-129">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="6e016-130">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6e016-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="6e016-131">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="6e016-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="6e016-132">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="6e016-132">System administrator</span></span>

- <span data-ttu-id="6e016-133">บริษัทต้องตั้งค่าเป็น **DEMF**</span><span class="sxs-lookup"><span data-stu-id="6e016-133">The company must be set to **DEMF**.</span></span>

- <span data-ttu-id="6e016-134">ทําตามขั้นตอนใน [ภาคผนวก 1](#appendix1) ของหัวข้อนี้ เพื่อดาวน์โหลดส่วนประกอบของโซลูชัน Microsoft ER ที่จําเป็นเพื่อประมวลผลการชําระเงินให้แก่ผู้จัดจําหน่าย</span><span class="sxs-lookup"><span data-stu-id="6e016-134">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the Microsoft ER solution that are required to process vendor payments.</span></span>
- <span data-ttu-id="6e016-135">ทําตามขั้นตอนใน [ภาคผนวก 2](#appendix2) ของหัวข้อนี้ เพื่อจัดเตรียมบัญชีเจ้าหนี้สําหรับการประมวลผลการชําระเงินของผู้จัดจําหน่าย โดยใช้โซลูชัน ER ที่คุณจะดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="6e016-135">Follow the steps in [Appendix 2](#appendix2) of this topic to prepare Accounts payable for vendor payment processing by using the ER solution that you will download.</span></span>

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a><span data-ttu-id="6e016-136">ประมวลผลการชําระเงินให้แก่ผู้จัดจําหน่ายเพื่อรับไฟล์การชําระเงิน</span><span class="sxs-lookup"><span data-stu-id="6e016-136">Process a vendor payment to get a payment file</span></span>

1. <span data-ttu-id="6e016-137">ทําตามขั้นตอนใน [ภาคผนวก 3](#appendix3) ของหัวข้อนี้ เพื่อประมวลผลการชําระเงินให้แก่ผู้จัดจําหน่าย</span><span class="sxs-lookup"><span data-stu-id="6e016-137">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>

    ![การประมวลผลการชําระเงินให้แก่ผู้จัดจําหน่ายอยู่ระหว่างการดำเนินการ](./media/er-data-debugger-process-payment.png)

2. <span data-ttu-id="6e016-139">ดาวน์โหลดและบันทึกไฟล์ zip ลงในคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6e016-139">Download and save the zip file to your local computer.</span></span>
3. <span data-ttu-id="6e016-140">แยกไฟล์การชําระเงิน **ISO20022 Credit transfer.xml** จากไฟล์ zip</span><span class="sxs-lookup"><span data-stu-id="6e016-140">Extract the **ISO20022 Credit transfer.xml** payment file from the zip file.</span></span>
4. <span data-ttu-id="6e016-141">เปิดไฟล์การชําระเงินที่แยกออกมา โดยใช้ตัวแสดงไฟล์ XML</span><span class="sxs-lookup"><span data-stu-id="6e016-141">Open the extracted payment file by using the XML file viewer.</span></span>

    <span data-ttu-id="6e016-142">ในไฟล์การชําระเงิน รหัสหมายเลขบัญชีธนาคารระหว่างประเทศ (IBAN) ของบัญชีธนาคารของผู้จัดจําหน่ายไม่มีช่องว่าง</span><span class="sxs-lookup"><span data-stu-id="6e016-142">In the payment file, the International Bank Account Number (IBAN) code of the vendor bank account contains no spaces.</span></span> <span data-ttu-id="6e016-143">ดังนั้น จะแตกต่างจากค่าที่ถูก [ป้อน](#enteredIBANcode) บนหน้า **บัญชีธนาคาร**</span><span class="sxs-lookup"><span data-stu-id="6e016-143">Therefore, it differs from the value that was [entered](#enteredIBANcode) on the **Bank accounts** page.</span></span>

    ![รหัส IBAN ไม่มีช่องว่าง](./media/er-data-debugger-payment-file.png)

    <span data-ttu-id="6e016-145">คุณสามารถใช้ดีบักเกอร์แหล่งข้อมูล ER เพื่อเรียนรู้ว่าส่วนประกอบของโซลูชัน ER ใดที่จะถูกใช้เพื่อตัดช่องว่างในรหัส IBAN</span><span class="sxs-lookup"><span data-stu-id="6e016-145">You can use the ER data source debugger to learn which component of the ER solution is used to truncate spaces in the IBAN code.</span></span>

## <a name="turn-on-data-source-debugging"></a><span data-ttu-id="6e016-146">เปิดการดีบักแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6e016-146">Turn on data source debugging</span></span>

1. <span data-ttu-id="6e016-147">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="6e016-147">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="6e016-148">ในหน้า **การตั้งค่าคอนฟิก** บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** ในกลุ่ม **การตั้งค่าล่วงหน้า** เลือก **พารามิเตอร์ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="6e016-148">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="6e016-149">ตั้งค่าตัวเลือก **เปิดใช้งานการดีบักข้อมูลเมื่อเรียกใช้รูปแบบ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="6e016-149">Set the **Enable data debugging at format run** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6e016-150">พารามิเตอร์นี้เฉพาะผู้ใช้และเฉพาะบริษัท</span><span class="sxs-lookup"><span data-stu-id="6e016-150">This parameter is user-specific and company-specific.</span></span>

    ![กล่องโต้ตอบพารามิเตอร์ผู้ใช้](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a><span data-ttu-id="6e016-152">ประมวลผลการชําระเงินให้แก่ผู้จัดจําหน่ายสําหรับการดีบัก</span><span class="sxs-lookup"><span data-stu-id="6e016-152">Process a vendor payment for debugging</span></span>

1. <span data-ttu-id="6e016-153">ทําตามขั้นตอนใน [ภาคผนวก 3](#appendix3) ของหัวข้อนี้ เพื่อประมวลผลการชําระเงินให้แก่ผู้จัดจําหน่าย</span><span class="sxs-lookup"><span data-stu-id="6e016-153">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>
2. <span data-ttu-id="6e016-154">ในกล่องข้อความ ให้เลือก **ใช่** เพื่อยืนยันว่าคุณต้องการยุติการประมวลผลการชําระเงินของผู้จัดจําหน่าย และเริ่มต้นการดีบักแหล่งข้อมูลแทนบนหน้า **ดีบักแหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="6e016-154">In the message box, select **Yes** to confirm that you want to interrupt vendor payment processing and instead start data source debugging on the **Debug Datasources** page.</span></span>

    ![กล่องข้อความการยืนยัน](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a><span data-ttu-id="6e016-156">ดีบักแหล่งข้อมูลที่ใช้ในการประมวลผลการชําระเงิน</span><span class="sxs-lookup"><span data-stu-id="6e016-156">Debug data sources that are used in payment processing</span></span>

### <a name="debug-the-model-mapping"></a><span data-ttu-id="6e016-157">ดีบักการแม็ปแบบจําลอง</span><span class="sxs-lookup"><span data-stu-id="6e016-157">Debug the model mapping</span></span>

1. <span data-ttu-id="6e016-158">บนหน้า **ดีบักแหล่งข้อมูล** บนบานหน้าต่างการดําเนินการ เลือก **การแม็ปแบบจําลอง** เพื่อเริ่มดีบักจากส่วนประกอบ ER นี้</span><span class="sxs-lookup"><span data-stu-id="6e016-158">On the **Debug Datasources** page, on the Action Pane, select **Model mapping** to start to debug from this ER component.</span></span>
2. <span data-ttu-id="6e016-159">ในบานหน้าต่างแหล่งข้อมูลทางด้านซ้าย ให้เลือกแหล่งข้อมูล **\$notSentTransactions** แล้วเลือก **อ่านเรกคอร์ดทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="6e016-159">In the data source pane on the left, select the **\$notSentTransactions** data source, and then select **Read all records**.</span></span>

    <span data-ttu-id="6e016-160">คุณสามารถเลือก **อ่าน 1 เรกคอร์ด** **อ่าน 10 เรกคอร์ด** **อ่าน 100 เรกคอร์ด** หรือ **อ่านเรกคอร์ดทั้งหมด** เพื่อบังคับให้มีการอ่านเรกคอร์ดจํานวนที่เหมาะสมจากแหล่งข้อมูลที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6e016-160">You can select **Read 1 record**, **Read 10 records**, **Read 100 records**, or **Read all records** to force the appropriate number of records to be read from the selected data source.</span></span> <span data-ttu-id="6e016-161">ด้วยวิธีนี้ คุณสามารถจําลองการเข้าถึงแหล่งข้อมูลจากรูปแบบ ER ที่เรียกใช้อยู่ได้</span><span class="sxs-lookup"><span data-stu-id="6e016-161">In this way, you can simulate access to the data source from the running ER format.</span></span>

3. <span data-ttu-id="6e016-162">ในบานหน้าต่างข้อมูลทางด้านขวา ให้เลือก **ขยายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="6e016-162">In the data pane on the right, select **Expand all**.</span></span>

    <span data-ttu-id="6e016-163">คุณจะเห็นว่าแหล่งข้อมูลที่เลือกของชนิด **รายการเรกคอร์ด** มีเรกคอร์ดเดียว</span><span class="sxs-lookup"><span data-stu-id="6e016-163">You can see that the selected data source of the **Record list** type contains a single record.</span></span>

4. <span data-ttu-id="6e016-164">ขยายแหล่งข้อมูล **\$notSentTransactions** และเลือกวิธีการ **vendBankAccountInTransactionCompany()** ที่ซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="6e016-164">Expand the **\$notSentTransactions** data source, and select the nested **vendBankAccountInTransactionCompany()** method.</span></span>
5. <span data-ttu-id="6e016-165">ขยายวิธีการ **vendBankAccountInTransactionCompany()** และเลือกฟิลด์ **IBAN** ที่ซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="6e016-165">Expand the **vendBankAccountInTransactionCompany()** method, and select the nested **IBAN** field.</span></span>
6. <span data-ttu-id="6e016-166">เลือก **รับค่า**</span><span class="sxs-lookup"><span data-stu-id="6e016-166">Select **Get value**.</span></span>

    <span data-ttu-id="6e016-167">คุณสามารถเลือก **รับค่า** เพื่อบังคับให้ค่าของฟิลด์ที่เลือกของแหล่งข้อมูลที่เลือกสามารถอ่านได้</span><span class="sxs-lookup"><span data-stu-id="6e016-167">You can select **Get value** to force the value of a selected field of the selected data source to be read.</span></span> <span data-ttu-id="6e016-168">ด้วยวิธีนี้ คุณสามารถจําลองการเข้าถึงฟิลด์นี้จากรูปแบบ ER ที่เรียกใช้อยู่ได้</span><span class="sxs-lookup"><span data-stu-id="6e016-168">In this way, you can simulate access to this field from the running ER format.</span></span>

7. <span data-ttu-id="6e016-169">เลือก **ขยายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="6e016-169">Select **Expand all**.</span></span>

    ![ค่าของฟิลด์ IBAN ในการแม็ปแบบจำลอง](./media/er-data-debugger-debugging-model-mapping.png)

    <span data-ttu-id="6e016-171">ดังเช่นที่คุณสามารถเห็นได้ การแม็ปแบบจําลองไม่รับผิดชอบพื้นที่ที่ถูกตัด เนื่องจากรหัส IBAN ที่ส่งกลับบัญชีธนาคารของผู้จัดจําหน่ายมีช่องว่าง</span><span class="sxs-lookup"><span data-stu-id="6e016-171">As you can see, the model mapping isn't responsible for the truncated spaces, because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="6e016-172">ดังนั้น คุณต้องดําเนินการดีบักแหล่งข้อมูลต่อไป</span><span class="sxs-lookup"><span data-stu-id="6e016-172">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format-mapping"></a><span data-ttu-id="6e016-173">ดีบักการแม็ปรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="6e016-173">Debug the format mapping</span></span>

1. <span data-ttu-id="6e016-174">บนหน้า **ดีบักแหล่งข้อมูล** บนบานหน้าต่างการดําเนินการ เลือก **การแม็ปรูปแบบ** เพื่อดําเนินการดีบักจากส่วนประกอบ ER นี้ต่อไป</span><span class="sxs-lookup"><span data-stu-id="6e016-174">On the **Debug Datasources** page, on the Action Pane, select **Format mapping** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="6e016-175">เลือกแหล่งข้อมูล **\$PaymentByDebtor** แล้วเลือก **อ่านเรกคอร์ดทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="6e016-175">Select the **\$PaymentByDebtor** data source, and then select **Read all records**.</span></span>
3. <span data-ttu-id="6e016-176">ขยาย **\$PaymentByDebtor**</span><span class="sxs-lookup"><span data-stu-id="6e016-176">Expand **\$PaymentByDebtor**.</span></span>
4. <span data-ttu-id="6e016-177">ขยาย **\$PaymentByDebtor.Lines** แล้วเลือก **อ่านเรกคอร์ดทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="6e016-177">Expand **\$PaymentByDebtor.Lines**, and then select **Read all records**.</span></span>
5. <span data-ttu-id="6e016-178">ขยาย **\$PaymentByDebtor.Lines.CreditorAccount**</span><span class="sxs-lookup"><span data-stu-id="6e016-178">Expand **\$PaymentByDebtor.Lines.CreditorAccount**.</span></span>
6. <span data-ttu-id="6e016-179">ขยาย **\$PaymentByDebtor.Lines.CreditorAccount.Identification** แล้วเลือก **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**</span><span class="sxs-lookup"><span data-stu-id="6e016-179">Expand **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, and then select **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span></span>
7. <span data-ttu-id="6e016-180">เลือก **รับค่า**</span><span class="sxs-lookup"><span data-stu-id="6e016-180">Select **Get value**.</span></span>
8. <span data-ttu-id="6e016-181">เลือก **ขยายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="6e016-181">Select **Expand all**.</span></span>

    ![ค่าของฟิลด์ IBAN ในการแม็ปรูปแบบ](./media/er-data-debugger-debugging-format-mapping.png)

    <span data-ttu-id="6e016-183">ดังเช่นที่คุณสามารถเห็นได้ แหล่งข้อมูลของรูปแบบไม่รับผิดชอบพื้นที่ที่ถูกตัด เนื่องจากรหัส IBAN ที่ส่งกลับบัญชีธนาคารของผู้จัดจําหน่ายมีช่องว่าง</span><span class="sxs-lookup"><span data-stu-id="6e016-183">As you can see, the data sources of the format mapping aren't responsible for the truncated spaces, because the IBAN code that they return for the vendor bank account includes spaces.</span></span> <span data-ttu-id="6e016-184">ดังนั้น คุณต้องดําเนินการดีบักแหล่งข้อมูลต่อไป</span><span class="sxs-lookup"><span data-stu-id="6e016-184">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format"></a><span data-ttu-id="6e016-185">ดีบักรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="6e016-185">Debug the format</span></span>

1. <span data-ttu-id="6e016-186">บนหน้า **ดีบักแหล่งข้อมูล** บนบานหน้าต่างการดําเนินการ เลือก **รูปแบบ** เพื่อดําเนินการดีบักจากส่วนประกอบ ER นี้ต่อไป</span><span class="sxs-lookup"><span data-stu-id="6e016-186">On the **Debug Datasources** page, on the Action Pane, select **Format** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="6e016-187">ขยายองค์ประกอบรูปแบบเพื่อเลือก **ISO20022CTReports** \> **XMLHeader** \> **เอกสาร** \> **CstmrCdtrfInitn** \> **Pmtinf** แล้วเลือก **อ่านเรกคอร์ดทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="6e016-187">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf**, and then select **Read all records**.</span></span>
3. <span data-ttu-id="6e016-188">ขยายองค์ประกอบรูปแบบเพื่อเลือก **ISO20022CTReports** \> **XMLHeader** \> **เอกสารt** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** แล้วเลือก **อ่านเรกคอร์ดทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="6e016-188">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, and then select **Read all records**.</span></span>
4. <span data-ttu-id="6e016-189">ขยายองค์ประกอบรูปแบบเพื่อเลือก **ISO20022CTReports** \> **XMLHeader** \> **เอกสาร** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** แล้วเลือก **รับค่า**</span><span class="sxs-lookup"><span data-stu-id="6e016-189">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, and then select **Get value**.</span></span>
5. <span data-ttu-id="6e016-190">เลือก **ขยายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="6e016-190">Select **Expand all**.</span></span>

    ![ค่าของฟิลด์ IBAN ในรูปแบบ](./media/er-data-debugger-debugging-format.png)

   <span data-ttu-id="6e016-192">ดังเช่นที่คุณสามารถเห็นได้ การผูกรูปแบบไม่รับผิดชอบพื้นที่ที่ถูกตัด เนื่องจากรหัส IBAN ที่ส่งกลับบัญชีธนาคารของผู้จัดจําหน่ายมีช่องว่าง</span><span class="sxs-lookup"><span data-stu-id="6e016-192">As you can see, the format binding isn't responsible for the truncated spaces because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="6e016-193">ดังนั้น องค์ประกอบ **BankIBAN** ถูกตั้งค่าคอนฟิกให้ใช้การแปลงรูปแบบที่ตัดทอนช่องว่าง</span><span class="sxs-lookup"><span data-stu-id="6e016-193">Therefore, the **BankIBAN** element is configured to use a format transformation that truncates spaces.</span></span>

6. <span data-ttu-id="6e016-194">ปิดดีบักเกอร์แหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6e016-194">Close the data source debugger.</span></span>

### <a name="review-the-format-transformations"></a><span data-ttu-id="6e016-195">ตรวจทานการแปลงรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="6e016-195">Review the format transformations</span></span>

1. <span data-ttu-id="6e016-196">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="6e016-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="6e016-197">บนหน้า **การตั้งค่าคอนฟิก** ให้เลือก **รูปแบบการชําระเงิน** \> **การโอนย้ายเครดิต ISO20022**</span><span class="sxs-lookup"><span data-stu-id="6e016-197">On the **Configurations** page, select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="6e016-198">เลือก **โปรแกรมออกแบบ** และจากนั้นขยายองค์ประกอบเพื่อเลือก **เอกสาร** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**</span><span class="sxs-lookup"><span data-stu-id="6e016-198">Select **Designer**, and then expand the elements to select **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span></span>

    ![องค์ประกอบ BankIBAN บนหน้าโปรแกรมออกแบบรูปแบบ](./media/er-data-debugger-referred-transformation.png)

    <span data-ttu-id="6e016-200">ดังเช่นที่คุณสามารถเห็นได้ องค์ประกอบ **BankIBAN** ถูกตั้งค่าคอนฟิกให้ใช้การแปลงข้อมูล **ลบที่ไม่ใช่ตัวอักษรและตัวเลข**</span><span class="sxs-lookup"><span data-stu-id="6e016-200">As you can see, the **BankIBAN** element is configured to use the **remove not alphanumeric** transformation.</span></span>

4. <span data-ttu-id="6e016-201">เลือกแท็บ **การแปลงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="6e016-201">Select the **Transformations** tab.</span></span>

    ![แท็บการแปลงสําหรับองค์ประกอบ BankIBAN](./media/er-data-debugger-transformation.png)

    <span data-ttu-id="6e016-203">ดังเช่นที่คุณสามารถเห็นได้ การแปลง **ลบที่ไม่ใช่ตัวอักษรและตัวเลข** ถูกตั้งค่าคอนฟิกให้ใช้นิพจน์ที่ตัดทอนช่องว่างจากสตริงข้อความที่ให้ไว้</span><span class="sxs-lookup"><span data-stu-id="6e016-203">As you can see, the **remove not alphanumeric** transformation is configured to use an expression that truncates spaces from the text string that is provided.</span></span>

## <a name="start-to-debug-in-the-operation-designer"></a><span data-ttu-id="6e016-204">เริ่มดีบักในโปรแกรมออกแบบการดําเนินงาน</span><span class="sxs-lookup"><span data-stu-id="6e016-204">Start to debug in the Operation designer</span></span>

<span data-ttu-id="6e016-205">เมื่อคุณตั้งค่าคอนฟิกรุ่นแบบร่างของรูปแบบ ER ที่สามารถเรียกใช้ได้โดยตรงจากโปรแกรมออกแบบการดําเนินงาน คุณสามารถเข้าถึงดีบักเกอร์แหล่งข้อมูล โดยการเลือก **เริ่มการดีบัก** บนบานหน้าต่างการดําเนินการ</span><span class="sxs-lookup"><span data-stu-id="6e016-205">When you configure a draft version of the ER format that can be run directly from the Operation designer, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![ปุ่ม เริ่มการดีบัก บนหน้าโปรแกรมออกแบบรูปแบบ](./media/er-data-debugger-run-from-designer.png)

<span data-ttu-id="6e016-207">การแม็ปรูปแบบและส่วนประกอบของรูปแบบของรูปแบบ ER ที่กําลังแก้ไขจะพร้อมใช้งานสําหรับการดีบัก</span><span class="sxs-lookup"><span data-stu-id="6e016-207">The format mapping and format components of the ER format that is being edited are available for debugging.</span></span>

## <a name="start-to-debug-in-the-model-mapping-designer"></a><span data-ttu-id="6e016-208">เริ่มดีบักในโปรแกรมออกแบบการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="6e016-208">Start to debug in the Model mapping designer</span></span>

<span data-ttu-id="6e016-209">เมื่อคุณตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER ที่สามารถเรียกใช้ได้จากหน้า **การแม็ปแบบจำลอง** คุณสามารถเข้าถึงดีบักเกอร์แหล่งข้อมูล โดยการเลือก **เริ่มการดีบัก** บนบานหน้าต่างการดําเนินการ</span><span class="sxs-lookup"><span data-stu-id="6e016-209">When you configure an ER model mapping that can be run from the **Model mapping** page, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![ปุ่ม เริ่มการดีบัก บนหน้าโปรแกรมออกแบบการแม็ปแบบจำลอง](./media/er-data-debugger-run-from-designer-mapping.png)

<span data-ttu-id="6e016-211">ส่วนประกอบการแม็ปแบบจําลองของการแม็ป ER ที่กําลังแก้ไขจะพร้อมใช้งานสําหรับการดีบัก</span><span class="sxs-lookup"><span data-stu-id="6e016-211">The model mapping component of the ER mapping that is being edited is available for debugging.</span></span>

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a><span data-ttu-id="6e016-212">ภาคผนวก 1: รับโซลูชัน ER</span><span class="sxs-lookup"><span data-stu-id="6e016-212">Appendix 1: Get an ER solution</span></span>

### <a name="download-an-er-solution"></a><span data-ttu-id="6e016-213">ดาวน์โหลดโซลูชัน ER</span><span class="sxs-lookup"><span data-stu-id="6e016-213">Download an ER solution</span></span>

<span data-ttu-id="6e016-214">ถ้าคุณต้องการใช้โซลูชัน ER เพื่อสร้างไฟล์การชําระเงินทางอิเล็กทรอนิกส์สําหรับการชําระเงินของผู้จัดจําหน่ายที่มีการประมวลผล คุฯสามารถ [ดาวน์โหลด](download-electronic-reporting-configuration-lcs.md) รูปแบบการชำระเงิน ER **การโอนย้ายเครดิต ISO20022** ที่พร้อมใช้งานจากไลบรารีสินทรัพย์ที่ใช้ร่วมกันใน Microsoft Dynamics Lifecycle Services (LCS) หรือจากที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="6e016-214">If you want to use an ER solution to generate an electronic payment file for a vendor payment that is processed, you can [download](download-electronic-reporting-configuration-lcs.md) the **ISO20022 Credit transfer** ER payment format that is available from the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) or from the Global repository.</span></span>

![การนําเข้ารูปแบบการชําระเงิน ER บนหน้าที่เก็บการตั้งค่าคอนฟิก](./media/er-data-debugger-import-from-repo.png)

<span data-ttu-id="6e016-216">นอกเหนือจากรูปแบบ ER ที่เลือก [การตั้งค่าคอนฟิก](general-electronic-reporting.md#Configuration) ต่อไปนี้ต้องนําเข้าในอินสแตนซ์ของ Microsoft Dynamics 365 Finance ของคุณโดยอัตโนมัติ โดยเป็นส่วนหนึ่งของโซลูชัน ER **การโอนย้ายเครดิต ISO20022** :</span><span class="sxs-lookup"><span data-stu-id="6e016-216">In addition to the selected ER format, the following [configurations](general-electronic-reporting.md#Configuration) must be automatically imported into your Microsoft Dynamics 365 Finance instance as part of the **ISO20022 Credit transfer** ER solution:</span></span>

- <span data-ttu-id="6e016-217">**รูปแบบการชำระเงิน** [การตั้งค่าคอนฟิกแบบจำลองข้อมูล ER](general-electronic-reporting.md#DataModelComponent)</span><span class="sxs-lookup"><span data-stu-id="6e016-217">**Payment model** [ER data model configuration](general-electronic-reporting.md#DataModelComponent)</span></span>
- <span data-ttu-id="6e016-218">**การโอนย้ายเครดิต ISO20022** [การตั้งค่าคอนฟิกรูปแบบ ER](general-electronic-reporting.md#FormatComponentOutbound)</span><span class="sxs-lookup"><span data-stu-id="6e016-218">**ISO20022 Credit transfer** [ER format configuration](general-electronic-reporting.md#FormatComponentOutbound)</span></span>
- <span data-ttu-id="6e016-219">**การแม็ปแบบจำลองการชำระเงิน 1611** [การตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER](general-electronic-reporting.md#ModelMappingComponent)</span><span class="sxs-lookup"><span data-stu-id="6e016-219">**Payment model mapping 1611** [ER model mapping configuration](general-electronic-reporting.md#ModelMappingComponent)</span></span>
- <span data-ttu-id="6e016-220">การตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER ของ **การแม็ปแบบจำลองการชำระเงินไปยังจุดปลายทาง ISO20022**</span><span class="sxs-lookup"><span data-stu-id="6e016-220">**Payment model mapping to destination ISO20022** ER model mapping configuration</span></span>

<span data-ttu-id="6e016-221">คุณสามารถค้นหาการตั้งค่าคอนฟิกเหล่านี้ได้บนหน้า **การตั้งค่าคอนฟิก** ของกรอบงาน ER (**การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**)</span><span class="sxs-lookup"><span data-stu-id="6e016-221">You can find these configurations on the **Configurations** page of the ER framework (**Organization administration** \> **Electronic reporting** \> **Configurations**).</span></span>

![การตั้งค่าคอนฟิกที่นำเข้าบนหน้าการตั้งค่าคอนฟิก](./media/er-data-debugger-configurations.png)

<span data-ttu-id="6e016-223">ถ้ามีการตั้งค่าคอนฟิกที่แสดงไว้ก่อนหน้านี้ใด ๆ ในแผนภูมิการตั้งค่าคอนฟิก คุณต้องดาวน์โหลดจากไลบรารีสินทรัพย์ LCS ที่ใช้ร่วมกันด้วยตนเองในลักษณะเดียวกับที่คุณดาวน์โหลดรูปแบบการชําระเงิน ER **การโอนย้ายเครดิต ISO20022**</span><span class="sxs-lookup"><span data-stu-id="6e016-223">If any of the previously listed configurations are missing in the configuration tree, you must manually download them from the LCS Shared asset library in the same way that you downloaded the **ISO20022 Credit transfer** ER payment format.</span></span>

### <a name="analyze-the-downloaded-er-solution"></a><span data-ttu-id="6e016-224">วิเคราะห์โซลูชัน ER ที่ดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="6e016-224">Analyze the downloaded ER solution</span></span>

#### <a name="review-the-model-mapping"></a><span data-ttu-id="6e016-225">ตรวจทานการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="6e016-225">Review the model mapping</span></span>

1. <span data-ttu-id="6e016-226">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="6e016-226">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="6e016-227">เลือก **รูปแบบการชําระเงิน** \> **การแม็ปแบบจําลองการชําระเงิน 1611**</span><span class="sxs-lookup"><span data-stu-id="6e016-227">Select **Payment model** \> **Payment model mapping 1611**.</span></span>
3. <span data-ttu-id="6e016-228">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="6e016-228">Select **Designer**.</span></span>
4. <span data-ttu-id="6e016-229">เลือกเรกคอร์ดการแม็ป **การแม็ปรูปแบบการชำระเงิน CT ISO20022**</span><span class="sxs-lookup"><span data-stu-id="6e016-229">Select the **Payment model mapping ISO20022 CT** mapping record.</span></span>
5. <span data-ttu-id="6e016-230">เลือก **โปรแกรมออกแบบ** แล้วตรวจทานการแม็ปแบบจําลองที่เปิด</span><span class="sxs-lookup"><span data-stu-id="6e016-230">Select **Designer**, and then review the model mapping that is opened.</span></span>

    <span data-ttu-id="6e016-231">โปรดสังเกตว่าฟิลด์ **การชําระเงิน** ของแบบจําลองข้อมูลถูกผูกไว้กับแหล่งข้อมูล **\$notSentTransactions** ที่ส่งกลับรายการของบรรทัดการชําระเงินของผู้จัดจําหน่ายที่กําลังประมวลผล</span><span class="sxs-lookup"><span data-stu-id="6e016-231">Notice that the **Payments** field of the data model is bound to the **\$notSentTransactions** data source that returns the list of vendor payment lines that are being processed.</span></span>

    ![ฟิลด์การชําระเงินบนหน้าโปรแกรมออกแบบการแม็ปแบบจําลอง](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a><span data-ttu-id="6e016-233">ตรวจทานการแม็ปรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="6e016-233">Review the format mapping</span></span>

1. <span data-ttu-id="6e016-234">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="6e016-234">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="6e016-235">เลือก **รูปแบบการชําระเงิน** \> **การโอนย้ายเครดิต ISO20022**</span><span class="sxs-lookup"><span data-stu-id="6e016-235">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="6e016-236">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="6e016-236">Select **Designer**.</span></span>
4. <span data-ttu-id="6e016-237">บนแท็บ **การแม็ป** ให้ตรวจทานการแม็ปรูปแบบที่เปิด</span><span class="sxs-lookup"><span data-stu-id="6e016-237">On the **Mapping** tab, review the format mapping that is opened.</span></span>

    <span data-ttu-id="6e016-238">โปรดสังเกตว่า **เอกสาร** \> **CstmrCdtTrfInitn** \> องค์ประกอบ **PmtInf** ของ **ISO20022CTReports** \> ไฟล์ **XMLHeader** ถูกผูกไว้กับแหล่งข้อมูล **\$PaymentByDebtor** ที่ถูกตั้งค่าคอนฟิกเพื่อจัดกลุ่มเรกคอร์ดของฟิลด์ **การชำระเงิน** ของแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6e016-238">Notice that the **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** element of the **ISO20022CTReports** \> **XMLHeader** file is bound to the **\$PaymentByDebtor** data source that is configured to group records of the data model's **Payments** field.</span></span>

    ![องค์ประกอบ PmtInf บนหน้าโปรแกรมออกแบบรูปแบบ](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a><span data-ttu-id="6e016-240">ตรวจทานรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="6e016-240">Review the format</span></span>

1. <span data-ttu-id="6e016-241">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="6e016-241">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="6e016-242">เลือก **รูปแบบการชําระเงิน** \> **การโอนย้ายเครดิต ISO20022**</span><span class="sxs-lookup"><span data-stu-id="6e016-242">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="6e016-243">เลือก **โปรแกรมออกแบบ** แล้วตรวจทานรูปแบบที่เปิด</span><span class="sxs-lookup"><span data-stu-id="6e016-243">Select **Designer**, and then review the format that is opened.</span></span>

    <span data-ttu-id="6e016-244">โปรดสังเกตว่าองค์ประกอบรูปแบบภายใต้ **เอกสาร** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** ถูกกําหนดค่าให้ป้อนรหัส IBAN ของบัญชีผู้จัดจําหน่ายในไฟล์การชําระเงิน</span><span class="sxs-lookup"><span data-stu-id="6e016-244">Notice that the format element under **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** is configured to enter the IBAN code of the vendor account in the payment file.</span></span>

    ![องค์ประกอบ BankIBAN บนหน้าโปรแกรมออกแบบรูปแบบ](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a><span data-ttu-id="6e016-246">ภาคผนวก 2: ตั้งค่าคอนฟิกบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="6e016-246">Appendix 2: Configure Accounts payable</span></span>

### <a name="modify-a-vendor-property"></a><span data-ttu-id="6e016-247">ปรับเปลี่ยนคุณสมบัติของผู้จัดจําหน่าย</span><span class="sxs-lookup"><span data-stu-id="6e016-247">Modify a vendor property</span></span>

1. <span data-ttu-id="6e016-248">ไปที่ **บัญชีของเจ้าหนี้** \> **ผู้จัดจำหน่าย** \> **ผู้จัดจำหน่ายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="6e016-248">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="6e016-249">เลือกผู้จัดจำหน่าย **DE-01002** และจากนั้น บนบานหน้าต่างการดำเนินการ บนแท็บ **ผู้จัดจำหน่าย** ในกลุ่ม **ตั้งค่า** เลือก **บัญชีธนาคาร**</span><span class="sxs-lookup"><span data-stu-id="6e016-249">Select vendor **DE-01002**, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="6e016-250">บนแท็บด่วน **การระบุรหัสประจำตัว** ในฟิลด์ **IBAN** <a name="enteredIBANcode"></a>ให้ป้อน **GB33 BUKB 2020 1555 5555 55**</span><span class="sxs-lookup"><span data-stu-id="6e016-250">On the **Identification** FastTab, in the **IBAN** field, <a name="enteredIBANcode"></a>enter **GB33 BUKB 2020 1555 5555 55**.</span></span>
4. <span data-ttu-id="6e016-251">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6e016-251">Select **Save**.</span></span>

![ฟิลด์ IBAN จะตั้งค่าบนหน้าบัญชีธนาคารของผู้จัดจำหน่าย](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a><span data-ttu-id="6e016-253">ตั้งค่าวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="6e016-253">Set up a method of payment</span></span>

1. <span data-ttu-id="6e016-254">ไปที่ **บัญชีเจ้าหนี้** \> **การตั้งค่าการชำระเงิน** \> **วิธีการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="6e016-254">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="6e016-255">เลือกวิธีการชำระเงิน **SEPA CT**</span><span class="sxs-lookup"><span data-stu-id="6e016-255">Select the **SEPA CT** payment method.</span></span>
3. <span data-ttu-id="6e016-256">บนแท็บด่วน **รูปแบบไฟล์** ในส่วน **รูปแบบไฟล์** ให้ตั้งค่าตัวเลือก **รูปแบบการส่งออกทางอิเล็กทรอนิกส์ทั่วไป** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="6e016-256">On the **File formats** FastTab, in the **File formats** section, set the **Generic electronic Export format** option to **Yes**.</span></span>
4. <span data-ttu-id="6e016-257">ในฟิลด์ **การตั้งค่าคอนฟิกรูปแบบการส่งออก** ให้เลือกรูปแบบ ER **การโอนย้ายเครดิต ISO20022**</span><span class="sxs-lookup"><span data-stu-id="6e016-257">In the **Export format configuration** field, select the **ISO20022 Credit transfer** ER format.</span></span>
5. <span data-ttu-id="6e016-258">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6e016-258">Select **Save**.</span></span>

![การตั้งค่ารูปแบบไฟล์ในหน้าวิธีการชําระเงิน](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a><span data-ttu-id="6e016-260">เพิ่มรายการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="6e016-260">Add a vendor payment</span></span>

1. <span data-ttu-id="6e016-261">ไปที่ **บัญชีเจ้าหนี้** \> **การชำระเงิน** \> **สมุดรายวันการชำระเงินผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="6e016-261">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="6e016-262">เพิ่มสมุดรายวันการชำระเงินใหม่</span><span class="sxs-lookup"><span data-stu-id="6e016-262">Add a new payment journal.</span></span>
3. <span data-ttu-id="6e016-263">เลือก **บรรทัด** และเพิ่มบรรทัดการชําระเงินใหม่</span><span class="sxs-lookup"><span data-stu-id="6e016-263">Select **Lines**, and add a new payment line.</span></span>
4. <span data-ttu-id="6e016-264">ในฟิลด์ **บัญชี** ให้เลือกผู้จัดจำหน่าย **DE-01002**</span><span class="sxs-lookup"><span data-stu-id="6e016-264">In the **Account** field, select vendor **DE-01002**.</span></span>
5. <span data-ttu-id="6e016-265">ในฟิลด์ **เดบิต** ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="6e016-265">In the **Debit** field, enter a value.</span></span>
6. <span data-ttu-id="6e016-266">ในฟิลด์ **วิธีการชำระเงิน** ให้เลือก **SEPA CT**</span><span class="sxs-lookup"><span data-stu-id="6e016-266">In the **Method of payment** field, select **SEPA CT**.</span></span>
7. <span data-ttu-id="6e016-267">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6e016-267">Select **Save**.</span></span>

![การชําระเงินให้แก่ผู้จัดจําหน่ายที่เพิ่มบนหน้าการชําระเงินให้แก่ผู้จัดจําหน่าย](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a><span data-ttu-id="6e016-269">ภาคผนวก 3: ดำเนินการการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="6e016-269">Appendix 3: Process a vendor payment</span></span>

1. <span data-ttu-id="6e016-270">ไปที่ **บัญชีเจ้าหนี้** \> **การชำระเงิน** \> **สมุดรายวันการชำระเงินผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="6e016-270">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="6e016-271">บนหน้า **สมุดรายวันการชำระเงินให้แก่ผู้จัดจำหน่าย** เลือกสมุดรายวันการชำระเงินที่คุณเพิ่งสร้าง และจากนั้นเลือก **บรรทัด**</span><span class="sxs-lookup"><span data-stu-id="6e016-271">On the **Vendor payment journal** page, select the payment journal that you previously created, and then select **Lines**.</span></span>
3. <span data-ttu-id="6e016-272">เลือกรายการการชำระเงิน แล้วเลือก **สถานะการชำระเงิน** \> **ไม่มี**</span><span class="sxs-lookup"><span data-stu-id="6e016-272">Select the payment line, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="6e016-273">เลือก **สร้างการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="6e016-273">Select **Generate payments**.</span></span>
5. <span data-ttu-id="6e016-274">ในฟิลด์ **วิธีการชำระเงิน** ให้เลือก **SEPA CT**</span><span class="sxs-lookup"><span data-stu-id="6e016-274">In the **Method of payment** field, select **SEPA CT**.</span></span>
6. <span data-ttu-id="6e016-275">ในฟิลด์ **บัญชีธนาคาร** ให้เลือก **DEMF OPER**</span><span class="sxs-lookup"><span data-stu-id="6e016-275">In the **Bank account** field, select **DEMF OPER**.</span></span>
7. <span data-ttu-id="6e016-276">ในกล่องโต้ตอบ **สร้างการชําระเงิน** ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6e016-276">In the **Generate payments** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="6e016-277">ในกล่องโต้ตอบ **พารามิเตอร์ของรายงานทางอิเล็กทรอนิกส์** เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6e016-277">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
