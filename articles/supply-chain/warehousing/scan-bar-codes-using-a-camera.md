---
title: สแกนบาร์โค้ดโดยใช้กล้องในแอปคลังสินค้า
description: หัวข้อนี้จะอธิบายวิธีตั้งค่าแอปคลังสินค้าเพื่อที่จะสแกนบาร์โค้ด โดยใช้กล้องบนอุปกรณ์เคลื่อนที่
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: fd4818ab936e1c93000793da756c97df6d05b2a9
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530017"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-app"></a><span data-ttu-id="7fa5b-103">สแกนบาร์โค้ดโดยใช้กล้องในแอปคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="7fa5b-103">Scan bar codes using a camera in the warehouse app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7fa5b-104">หัวข้อนี้จะอธิบายวิธีตั้งค่าแอปคลังสินค้าเพื่อที่จะสแกนบาร์โค้ด โดยใช้กล้องบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="7fa5b-104">This topic explains how to set up the warehouse app to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="7fa5b-105">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="7fa5b-105">Prerequisites</span></span>
<span data-ttu-id="7fa5b-106">ในการใช้คุณลักษณะนี้ คุณต้องติดตั้งแอปคลังสินค้า รุ่น 1.2.0.0 และอุปกรณ์ของคุณต้องมีกล้อง</span><span class="sxs-lookup"><span data-stu-id="7fa5b-106">To use this feature, you need to have version 1.2.0.0 of the warehouse app installed, and your device must have a camera.</span></span> <span data-ttu-id="7fa5b-107">เมื่อคุณเปิดแอปหลังจากที่ได้อัพเดตแล้ว ระบบจะขอให้คุณอนุญาตให้แอพเข้าใช้กล้อง</span><span class="sxs-lookup"><span data-stu-id="7fa5b-107">When you open the app after updating, you will be prompted to allow the app to use the camera.</span></span> <span data-ttu-id="7fa5b-108">ถ้าอุปกรณ์ของคุณไม่มีกล้อง จะไม่มีการแสดงข้อความเตือน และคุณจะไม่สามารถใช้กล้องเป็นสแกนเนอร์ได้</span><span class="sxs-lookup"><span data-stu-id="7fa5b-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="7fa5b-109">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="7fa5b-109">Setup</span></span>
<span data-ttu-id="7fa5b-110">ในการตั้งค่าการแสดงผลของแอปลิเคชันคลังสินค้า คุณสามารถเลือกได้ว่า ควรจะใช้กล้องสำหรับการสแกนบาร์โค้ดหรือไม่</span><span class="sxs-lookup"><span data-stu-id="7fa5b-110">In the Display settings of the warehouse application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="7fa5b-111">ถ้าคุณเปิดใช้งาน **ใช้กล้องเป็นสแกนเนอร์** คุณสามารถใช้กล้องในทุกฟิลด์อินพุทที่มีโหมดอินพุทที่ต้องการ ซึ่งตั้งค่าเป็น **การสแกน** ได้</span><span class="sxs-lookup"><span data-stu-id="7fa5b-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="7fa5b-112">เพื่อควบคุมว่าฟิลด์ป้อนข้อมูลควรสามารถสแกนได้หรือไม่ ในหน้า **ชื่อฟิลด์แอพ Warehouse** ให้ตั้งค่า **วิธีการป้อนข้อมูลที่ต้องการ** เป็น **การสแกน**.</span><span class="sxs-lookup"><span data-stu-id="7fa5b-112">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="7fa5b-113">เมื่อมีการเลือกตัวเลือกนี้ คุณสามารถใช้กล้องสำหรับการสแกนในแอปคลังสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="7fa5b-113">When this option is selected, a camera can be used for scanning in the warehouse app.</span></span> <span data-ttu-id="7fa5b-114">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกชื่อฟิลด์ของแอปใน Warehousing ดู [ตั้งค่าคอนฟิกชื่อฟิลด์ของแอปในแอปคลังสินค้า](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse)</span><span class="sxs-lookup"><span data-stu-id="7fa5b-114">For information about how to configure app field names in Warehousing, see [Configure app field names in warehouse app](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="7fa5b-115">รูปแบบบาร์โค้ดที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="7fa5b-115">Supported bar code formats</span></span>
<span data-ttu-id="7fa5b-116">รูปบาร์โค้ดทั่วไปส่วนใหญ่ได้รับการสนับสนุน ซึ่งรวมถึงรหัส 128 รหัส 39 รหัส 93 EAN-8 EAN-13 UPC-E UPC-A และรหัส QR</span><span class="sxs-lookup"><span data-stu-id="7fa5b-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="7fa5b-117">การนำทาง</span><span class="sxs-lookup"><span data-stu-id="7fa5b-117">Navigation</span></span>
<span data-ttu-id="7fa5b-118">หน้ากล้องจะถูกเริ่มในแต่ละหน้าที่ฟิลด์อินพุทมีโหมดอินพุทที่ต้องการซึ่งถูกตั้งค่าเป็น การสแกน เมื่อคุณอยู่ที่หน้ากล้อง ให้ใช้ตัวเลือกต่อไปนี้เพื่อนำทาง:</span><span class="sxs-lookup"><span data-stu-id="7fa5b-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="7fa5b-119">คลิกปุ่มย้อนกลับเพื่อย้อนกลับไปยังหน้างานและรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="7fa5b-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="7fa5b-120">คลิกดินสอบนหน้างานและรายละเอียด เพื่อไปยังหน้าซึ่งคุณสามารถพิมพ์อินพุทได้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="7fa5b-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="7fa5b-121">คลิกกล้องบนหน้างานและรายละเอียดเพื่อย้อนกลับไปยังหน้ากล้อง</span><span class="sxs-lookup"><span data-stu-id="7fa5b-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="7fa5b-122">หน้างานและรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="7fa5b-122">Task and details page</span></span> | <span data-ttu-id="7fa5b-123">หน้ากล้อง</span><span class="sxs-lookup"><span data-stu-id="7fa5b-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![กล้อง การสแกน ตัวอย่าง งาน รายละเอียด หน้า](./media/camera-scanning-example-task-detail-page50.png)          | ![กล้อง การสแกน ตัวอย่าง กล้อง หน้า เล็กลง](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="7fa5b-126">บนหน้ากล้อง เมื่อคุณคลิกปุ่มกล้อง จะปรากฏเป็นจางลง ขณะที่พยายามระบุบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="7fa5b-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="7fa5b-127">ถ้าไม่มีการระบุบาร์โค้ดภายใน 5 วินาที กระบวนการจะหมดเวลา และปุ่มกล้องจะกลายเป็นพร้อมใช้งานอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="7fa5b-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="7fa5b-128">จากนั้น คุณจะสามารถลองสแกนบาร์โค้ดได้อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="7fa5b-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="7fa5b-129">เมื่อคุณหันกล้องไปที่บาร์โค้ด รักษาให้บาร์โค้ดอยู่ในระดับภายในเครื่องหมายวงเล็บเพื่อผลลัพธ์ที่ดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="7fa5b-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="7fa5b-130">เมื่อมีการสแกนบาร์โค้ดเสร็จเรียบร้อยแล้ว ผลลัพธ์จะถูกประมวลผล และคุณจะถูกนำไปยังขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="7fa5b-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="7fa5b-131">ถ้าขั้นตอนถัดไปประกอบด้วย ฟิลด์อินพุทอีกฟิลด์หนึ่งที่มีโหมดอินพุทที่ต้องการซึ่งถูกตั้งค่าเป็น การสแกน หน้ากล้องจะเริ่มต้นอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="7fa5b-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="7fa5b-132">ถ้าขั้นตอนถัดไปไม่ใช่ฟิลด์การสแกน จากนั้นหน้ากล้องจะไม่มีการเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="7fa5b-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>

