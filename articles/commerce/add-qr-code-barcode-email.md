---
title: เพิ่มQR code หรือบาร์โค้ดในอีเมลเกี่ยวกับธุรกรรมและใบเสร็จ
description: หัวข้อนี้อธิบายวิธีการแทรกQR code และบาร์โค้ดที่แสดงรหัสใบสั่งลงในอีเมลธุรกรรมและใบเสร็จใน Microsoft Dynamics 365 Commerce
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 9eea69f9618d4387f5d6320620dfee5d74813fc0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019550"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a><span data-ttu-id="74010-103">เพิ่มQR code หรือบาร์โค้ดในอีเมลเกี่ยวกับธุรกรรมและใบเสร็จ</span><span class="sxs-lookup"><span data-stu-id="74010-103">Add a QR code or bar code to transactional and receipt emails</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="74010-104">หัวข้อนี้อธิบายวิธีการแทรกQR code และบาร์โค้ดที่แสดงรหัสใบสั่งลงในอีเมลธุรกรรมและใบเสร็จใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="74010-104">This topic explains how to insert QR codes and bar codes that represent order IDs into transactional and receipt emails in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="74010-105">คุณสามารถรวม QR codes และบาร์โค้ดในอีเมลธุรกรรมได้อย่างง่ายดายเพื่อช่วยให้กระบวนการค้นหาใบสั่งในสภาพแวดล้อมการขายปลีกรวดเร็วขึ้น</span><span class="sxs-lookup"><span data-stu-id="74010-105">You can easily include QR codes and bar codes in transactional emails to help speed up the order lookup process in a retail environment.</span></span> <span data-ttu-id="74010-106">เมื่อต้องการแทรก QR codes และบาร์โค้ดลงในอีเมล ให้คุณใช้แท็ก HTML **\<img\>** ที่ขอ QR codes หรือรูปภาพบาร์โค้ดจากบริการสร้างและการแสดงผล</span><span class="sxs-lookup"><span data-stu-id="74010-106">To insert QR codes and bar codes into emails, you use an HTML **\<img\>** tag that requests a QR code or bar code image from a generation and rendering service.</span></span> <span data-ttu-id="74010-107">Microsoft ไม่ได้ให้บริการนี้</span><span class="sxs-lookup"><span data-stu-id="74010-107">Microsoft doesn't provide this service.</span></span> <span data-ttu-id="74010-108">อย่างไรก็ตาม มีการบริการฟรีหรือบริการที่ราคาไม่แพงอีกมากที่สามารถให้บริการ QR code หรือบาร์โค้ดที่สร้างขึ้นแบบไดนามิกตามค่าที่ส่งผ่านในสตริงการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="74010-108">However, there are many free or inexpensive services that can serve QR codes or bar codes that are dynamically generated based on a value that is passed in a query string.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a><span data-ttu-id="74010-109">เพิ่ม QR code หรือบาร์โค้ดในอีเมลเกี่ยวกับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="74010-109">Add a QR code or bar code to a transactional email</span></span>

<span data-ttu-id="74010-110">หากต้องการแทรก QR code หรือบาร์โค้ดลงในอีเมลธุรกรรมที่ถูกส่งเป็นส่วนหนึ่งของการซื้อโดย e-commerce ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="74010-110">To insert a QR code or bar code into a transactional email that is sent as part of an e-commerce purchase, follow these steps.</span></span>

1. <span data-ttu-id="74010-111">เปิด HTML ต้นทางจากเท็มเพลตอีเมลเชิงธุรกรรม และเพิ่มแท็ก HTML **\<img\>** ที่ชี้ไปยังบริการ QR code หรือบาร์โค้ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="74010-111">Open the source HTML for the transactional email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="74010-112">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="74010-112">Here is an example.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    <span data-ttu-id="74010-113">นี่เป็นคำอธิบายของของตัวอย่างก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="74010-113">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="74010-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** แสดงถึงโดเมนของบริการ QR code หรือบาร์โค้ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="74010-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="74010-115">**ข้อมูล** จะแสดงพารามิเตอร์ที่บริการ QR code หรือบาร์โค้ดใช้รับเนื้อหาที่ควรแสดงเป็น QR code หรือบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="74010-115">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="74010-116">ต้องมอบหมายค่า **%salesid%** ให้กับพารามิเตอร์นี้</span><span class="sxs-lookup"><span data-stu-id="74010-116">The value **%salesid%** must be assigned to this parameter.</span></span> <span data-ttu-id="74010-117">ในตัวอย่างนี้ ให้สังเกตว่าค่านี้จะใช้เป็นข้อความแสดงแทนของรูปภาพด้วย</span><span class="sxs-lookup"><span data-stu-id="74010-117">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="74010-118">**param1** และ **param2** จะแสดงถึงพารามิเตอร์ทางเลือกเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="74010-118">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="74010-119">ไปที่ **การค้าปลีกและการพาณิชย์ \> การตั้งค่าสำนักงานใหญ่ \> พารามิเตอร์ \> เทมเพลตอีเมลขององค์กร** และอัพโหลด HTML ล่าสุดลงในเทมเพลตอีเมลเชิงธุรกรรมที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="74010-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the appropriate transactional email template.</span></span>

> [!NOTE]
> <span data-ttu-id="74010-120">พารามิเตอร์อาจแตกต่างกันระหว่างผู้ให้บริการ QR code และบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="74010-120">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="74010-121">ดังนั้น โปรดติดต่อผู้ให้บริการของคุณเพื่อยืนยันพารามิเตอร์ที่คุณต้องกําหนดค่าให้</span><span class="sxs-lookup"><span data-stu-id="74010-121">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a><span data-ttu-id="74010-122">เพิ่ม QR code หรือบาร์โค้ดในอีเมลเกี่ยวกับใบเสร็จ</span><span class="sxs-lookup"><span data-stu-id="74010-122">Add a QR code or bar code to a receipt email</span></span> 

<span data-ttu-id="74010-123">หากต้องการแทรก QR code หรือบาร์โคดลงในอีเมลใบเสร็จที่สามารถส่งได้หลังจากที่ซื้อที่จุดขาย (POS) ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="74010-123">To insert a QR code or bar code into a receipt email that can be sent after a purchase is made at the point of sale (POS), follow these steps.</span></span>

1. <span data-ttu-id="74010-124">เปิด HTML ต้นทางสำหรับเทมเพลตอีเมลใบเสร็จ และเพิ่มแท็ก HTML **\<img\>** ที่ชี้ไปยังบริการ QR code หรือบาร์โค้ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="74010-124">Open the source HTML for the receipt email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="74010-125">ดูตัวอย่างได้จากด้านล่างนี้</span><span class="sxs-lookup"><span data-stu-id="74010-125">Here is an example below.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    <span data-ttu-id="74010-126">นี่เป็นคำอธิบายของของตัวอย่างก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="74010-126">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="74010-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** แสดงถึงโดเมนของบริการ QR code หรือบาร์โค้ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="74010-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="74010-128">**ข้อมูล** จะแสดงพารามิเตอร์ที่บริการ QR code หรือบาร์โค้ดใช้รับเนื้อหาที่ควรแสดงเป็น QR code หรือบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="74010-128">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="74010-129">ต้องมอบหมายค่า **%receiptid%** ให้กับพารามิเตอร์นี้</span><span class="sxs-lookup"><span data-stu-id="74010-129">The value **%receiptid%** must be assigned to this parameter.</span></span> <span data-ttu-id="74010-130">ในตัวอย่างนี้ ให้สังเกตว่าค่านี้จะใช้เป็นข้อความแสดงแทนของรูปภาพด้วย</span><span class="sxs-lookup"><span data-stu-id="74010-130">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="74010-131">**param1** และ **param2** จะแสดงถึงพารามิเตอร์ทางเลือกเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="74010-131">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="74010-132">ไปที่ **การค้าปลีกและการพาณิชย์ \> การตั้งค่าสำนักงานใหญ่ \> พารามิเตอร์ \> เทมเพลตอีเมลขององค์กร** และอัพโหลด HTML ล่าสุดลงในเทมเพลตอีเมลที่มีรหัสอีเมล์ **emailrecpt**</span><span class="sxs-lookup"><span data-stu-id="74010-132">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the email template that has the email ID **emailrecpt**.</span></span>

> [!NOTE]
> <span data-ttu-id="74010-133">พารามิเตอร์อาจแตกต่างกันระหว่างผู้ให้บริการ QR code และบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="74010-133">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="74010-134">ดังนั้น โปรดติดต่อผู้ให้บริการของคุณเพื่อยืนยันพารามิเตอร์ที่คุณต้องกําหนดค่าให้</span><span class="sxs-lookup"><span data-stu-id="74010-134">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="74010-135">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="74010-135">Additional resources</span></span>

[<span data-ttu-id="74010-136">ส่งใบเสร็จทางอีเมลจาก Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="74010-136">Send email receipts from Modern POS (MPOS)</span></span>](email-receipts.md)

[<span data-ttu-id="74010-137">สร้างเท็มเพลตอีเมลสำหรับเหตุการณ์ของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="74010-137">Create email templates for transactional events</span></span>](email-templates-transactions.md)
