---
title: สแกนบาร์โค้ดโดยใช้กล้องใน Dynamics 365 for Finance and Operations – คลังสินค้า
description: หัวข้อนี้อธิบายวิธีการตั้งค่า Dynamics 365 for Finance and Operations – คลังสินค้าที่จะสแกนบาร์โค้ดโดยใช้กล้องบนอุปกรณ์มือถือ
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 5ec9197c2e8b7970fcbf5ea42612c60f940bcae0
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742945"
---
# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-for-finance-and-operations--warehousing"></a><span data-ttu-id="cb91e-103">สแกนบาร์โค้ดโดยใช้กล้องใน Dynamics 365 for Finance and Operations – คลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cb91e-103">Scan bar codes using a camera in Dynamics 365 for Finance and Operations – Warehousing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb91e-104">หัวข้อนี้อธิบายวิธีการตั้งค่า Dynamics 365 for Finance and Operations – คลังสินค้าที่จะสแกนบาร์โค้ดโดยใช้กล้องบนอุปกรณ์มือถือ</span><span class="sxs-lookup"><span data-stu-id="cb91e-104">This topic explains how to set up Dynamics 365 for Finance and Operations – Warehousing to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="cb91e-105">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="cb91e-105">Prerequisites</span></span>
<span data-ttu-id="cb91e-106">ในการใช้คุณลักษณะนี้ คุณต้องมี Warehousing รุ่น 1.2.0.0 ที่ติดตั้งอยู่ และอุปกรณ์ของคุณต้องมีกล้อง</span><span class="sxs-lookup"><span data-stu-id="cb91e-106">To use this feature, you need to have version 1.2.0.0 of Warehousing installed, and your device must have a camera.</span></span> <span data-ttu-id="cb91e-107">เมื่อคุณเปิดแอปหลังจากการปรับปรุง คุณจะได้รับการพร้อมท์ให้อนุญาต Dynamics 365 for Finance and Operations – แอพลิเคชันคลังสินค้าที่จะใช้กล้อง</span><span class="sxs-lookup"><span data-stu-id="cb91e-107">When you open the app after updating, you will be prompted to allow the Dynamics 365 for Finance and Operations – Warehousing application to use the camera.</span></span> <span data-ttu-id="cb91e-108">ถ้าอุปกรณ์ของคุณไม่มีกล้อง จะไม่มีการแสดงข้อความเตือน และคุณจะไม่สามารถใช้กล้องเป็นสแกนเนอร์ได้</span><span class="sxs-lookup"><span data-stu-id="cb91e-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="cb91e-109">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="cb91e-109">Setup</span></span>
<span data-ttu-id="cb91e-110">ในการตั้งค่าการแสดงของแอพลิเคชัน Warehousing คุณสามารถเลือกได้ว่า กล้องควรจะใช้สำหรับการสแกนบาร์โค้ดหรือไม่</span><span class="sxs-lookup"><span data-stu-id="cb91e-110">In the Display settings of the Warehousing application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="cb91e-111">ถ้าคุณเปิดใช้งาน **ใช้กล้องเป็นสแกนเนอร์** คุณสามารถใช้กล้องในทุกฟิลด์อินพุทที่มีโหมดอินพุทที่ต้องการ ซึ่งตั้งค่าเป็น **การสแกน** ได้</span><span class="sxs-lookup"><span data-stu-id="cb91e-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="cb91e-112">เพื่อควบคุมว่าฟิลด์ป้อนเข้าควรสามารถสแกนได้หรือไม่ ในหน้า **ชื่อฟิลด์แอปคลังสินค้า** ใน Dynamics 365 for Finance and Operations ตั้งค่า **โหมดขาเข้าที่ต้องการ** เป็น **การสแกน**</span><span class="sxs-lookup"><span data-stu-id="cb91e-112">To control whether an input field should be scannable, on the **Warehouse app field names** page in Dynamics 365 for Finance and Operations, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="cb91e-113">เมื่อมีการเลือกตัวเลือกนี้ คุณสามารถใช้กล้องสำหรับการสแกนในแอพลิเคชัน Warehousing ได้</span><span class="sxs-lookup"><span data-stu-id="cb91e-113">When this option is selected, a camera can be used for scanning in the Warehousing app.</span></span> <span data-ttu-id="cb91e-114">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกชื่อฟิลด์แอพลิเคชันใน Warehousing ดู [ตั้งค่าคอนฟิกชื่อฟิลด์แอพลิเคชันในแอพลิเคชัน Warehousing](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse)</span><span class="sxs-lookup"><span data-stu-id="cb91e-114">For information about how to configure app field names in Warehousing, see [Configure app field names in Warehousing app](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="cb91e-115">รูปแบบบาร์โค้ดที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="cb91e-115">Supported bar code formats</span></span>
<span data-ttu-id="cb91e-116">รูปบาร์โค้ดทั่วไปส่วนใหญ่ได้รับการสนับสนุน ซึ่งรวมถึงรหัส 128 รหัส 39 รหัส 93 EAN-8 EAN-13 UPC-E UPC-A และรหัส QR</span><span class="sxs-lookup"><span data-stu-id="cb91e-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="cb91e-117">การนำทาง</span><span class="sxs-lookup"><span data-stu-id="cb91e-117">Navigation</span></span>
<span data-ttu-id="cb91e-118">หน้ากล้องจะถูกเริ่มในแต่ละหน้าที่ฟิลด์อินพุทมีโหมดอินพุทที่ต้องการซึ่งถูกตั้งค่าเป็น การสแกน เมื่อคุณอยู่ที่หน้ากล้อง ให้ใช้ตัวเลือกต่อไปนี้เพื่อนำทาง:</span><span class="sxs-lookup"><span data-stu-id="cb91e-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="cb91e-119">คลิกปุ่มย้อนกลับเพื่อย้อนกลับไปยังหน้างานและรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="cb91e-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="cb91e-120">คลิกดินสอบนหน้างานและรายละเอียด เพื่อไปยังหน้าซึ่งคุณสามารถพิมพ์อินพุทได้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="cb91e-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="cb91e-121">คลิกกล้องบนหน้างานและรายละเอียดเพื่อย้อนกลับไปยังหน้ากล้อง</span><span class="sxs-lookup"><span data-stu-id="cb91e-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="cb91e-122">หน้างานและรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="cb91e-122">Task and details page</span></span> | <span data-ttu-id="cb91e-123">หน้ากล้อง</span><span class="sxs-lookup"><span data-stu-id="cb91e-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![กล้อง-การสแกน-ตัวอย่าง-งาน-รายละเอียด-หน้า](./media/camera-scanning-example-task-detail-page50.png)          | ![กล้อง-การสแกน-ตัวอย่าง-กล้อง-หน้า-เล็กกว่า](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="cb91e-126">บนหน้ากล้อง เมื่อคุณคลิกปุ่มกล้อง จะปรากฏเป็นจางลง ขณะที่พยายามระบุบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="cb91e-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="cb91e-127">ถ้าไม่มีการระบุบาร์โค้ดภายใน 5 วินาที กระบวนการจะหมดเวลา และปุ่มกล้องจะกลายเป็นพร้อมใช้งานอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="cb91e-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="cb91e-128">จากนั้น คุณจะสามารถลองสแกนบาร์โค้ดได้อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="cb91e-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="cb91e-129">เมื่อคุณหันกล้องไปที่บาร์โค้ด รักษาให้บาร์โค้ดอยู่ในระดับภายในเครื่องหมายวงเล็บเพื่อผลลัพธ์ที่ดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="cb91e-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="cb91e-130">เมื่อมีการสแกนบาร์โค้ดเสร็จเรียบร้อยแล้ว ผลลัพธ์จะถูกประมวลผล และคุณจะถูกนำไปยังขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="cb91e-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="cb91e-131">ถ้าขั้นตอนถัดไปประกอบด้วย ฟิลด์อินพุทอีกฟิลด์หนึ่งที่มีโหมดอินพุทที่ต้องการซึ่งถูกตั้งค่าเป็น การสแกน หน้ากล้องจะเริ่มต้นอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="cb91e-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="cb91e-132">ถ้าขั้นตอนถัดไปไม่ใช่ฟิลด์การสแกน จากนั้นหน้ากล้องจะไม่มีการเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="cb91e-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>

