---
title: ระบุตำแหน่งที่ตั้งของที่เก็บข้อมูลที่กำหนดเองสำหรับเอกสารที่จัดทำ
description: หัวข้อนี้อธิบายวิธีการขยายรายการของสถานที่เก็บสำหรับเอกสารที่รูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) สร้างขึ้น
author: NickSelin
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bd979bf5369b6878caaee82fc9c6a40d363cc165
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894159"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a><span data-ttu-id="794d5-103">ระบุตำแหน่งที่ตั้งของที่เก็บข้อมูลที่กำหนดเองสำหรับเอกสารที่จัดทำ</span><span class="sxs-lookup"><span data-stu-id="794d5-103">Specify custom storage locations for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="794d5-104">Application Programming Interface (API) ของกรอบงานการรายงานทางอิเล็กทรอนิกส์ (ER) ช่วยให้คุณสามารถขยายรายการของสถานที่เก็บสำหรับเอกสารที่รูปแบบ ER สร้าง</span><span class="sxs-lookup"><span data-stu-id="794d5-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="794d5-105">หัวข้อนี้จะอธิบายถึงวิธีการเพิ่มสถานที่เก็บที่กำหนดเองสำหรับเอกสารที่สร้างขึ้นโดยการมอบหมายงานของการสร้างปลายทาง ER ให้กับโรงงานปลายทางเริ่มต้นแล้วใช้คลาสที่กำหนดเองที่มีตรรกะปลายทางของตนเอง</span><span class="sxs-lookup"><span data-stu-id="794d5-105">This topic explains how to add a custom storage location for generated documents by delegating the task of creating ER destinations to the default destination factory and then implementing a custom class that has its own destination logic.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="794d5-106">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="794d5-106">Prerequisites</span></span>

<span data-ttu-id="794d5-107">ปรับใช้โทโพโลยีที่สนับสนุนการสร้างแบบต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="794d5-107">Deploy a topology that supports continuous build.</span></span> <span data-ttu-id="794d5-108">สำหรับข้อมูลเพิ่มเติม ดู [ปรับใช้โทโพโลยีซึ่งสนับสนุนการสร้างอย่างต่อเนื่องและระบบอัตโนมัติของการทดสอบ](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation)</span><span class="sxs-lookup"><span data-stu-id="794d5-108">For more information, see [Deploy topologies that support continuous build and test automation](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).</span></span> <span data-ttu-id="794d5-109">คุณต้องมีการเข้าถึงโทโพโลยีนี้สำหรับหนึ่งในบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="794d5-109">You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="794d5-110">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="794d5-110">Electronic reporting developer</span></span>
- <span data-ttu-id="794d5-111">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="794d5-111">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="794d5-112">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="794d5-112">System administrator</span></span>

<span data-ttu-id="794d5-113">คุณต้องมีการเข้าถึงไปยังสภาพแวดล้อมการพัฒนาสำหรับโทโพโลยีนี้</span><span class="sxs-lookup"><span data-stu-id="794d5-113">You must also have access to the development environment for this topology.</span></span>

<span data-ttu-id="794d5-114">คุณสามารถดำเนินงานทั้งหมดในหัวข้อนี้ให้เสร็จสมบูรณ์ได้ในบริษัท **USMF**</span><span class="sxs-lookup"><span data-stu-id="794d5-114">All the tasks in this topic can be completed in the **USMF** company.</span></span>

## <a name="import-the-fixed-asset-roll-forward-er-format"></a><span data-ttu-id="794d5-115">นำเข้ารูปแบบ ER การกระทบยอดสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="794d5-115">Import the Fixed asset roll forward ER format</span></span>

<span data-ttu-id="794d5-116">เมื่อต้องการสร้างเอกสารที่คุณต้องการเพิ่มที่ตั้งที่จัดเก็บแบบกำหนดเอง สำหรับ [การนำเข้า](er-download-configurations-global-repo.md) ตั้งค่าคอนฟิกรูปแบบ ER **การกระทบยอดสินทรัพย์ถาวร** ในโทโพโลยีปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="794d5-116">To generate the documents that you plan to add a custom storage location for, [import](er-download-configurations-global-repo.md) the **Fixed asset roll forward** ER format configuration into the current topology.</span></span>

![หน้าที่เก็บการตั้งค่าคอนฟิก](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="794d5-118">เรียกใช้รายงานการกระทบยอดสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="794d5-118">Run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="794d5-119">ไปที่ **สินทรัพย์ถาวร** \> **การสอบถามและรายงาน** \> **รายงานธุรกรรม** \> **การกระทบยอดสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="794d5-119">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="794d5-120">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่ **1/1/2017** (มกราคม 1 2017)</span><span class="sxs-lookup"><span data-stu-id="794d5-120">In the **From date** field, enter **1/1/2017** (January 1, 2017).</span></span>
3. <span data-ttu-id="794d5-121">ในฟิลด์ **วันที่นื้สิ้นสุด** ให้ป้อนวันที่ **1/31/2017** (มกราคม 31 2017)</span><span class="sxs-lookup"><span data-stu-id="794d5-121">In the **To date** field, enter **1/31/2017** (January 31, 2017).</span></span>
4. <span data-ttu-id="794d5-122">ใน **ฟิลด์สกุลเงิน** ให้เลือก **สกุลเงินการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="794d5-122">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="794d5-123">ในฟิลด์ **รูปแบบการแม็ป** ให้เลือก **การกระทบยอดสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="794d5-123">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="794d5-124">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="794d5-124">Select **OK**.</span></span>

![กล่องโต้ตอบรันไทม์สำหรับรายงานการกระทบยอดสินทรัพย์ถาวร](./media/er-custom-storage-generated-files-runtime-dialog.png)

<span data-ttu-id="794d5-126">ใน Microsoft Excel ให้ตรวจสอบเอกสารขาออกที่สร้างขึ้นและพร้อมใช้งานสำหรับการดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="794d5-126">In Microsoft Excel, review the outbound document that is generated and available for download.</span></span> <span data-ttu-id="794d5-127">ลักษณะการทำงานนี้เป็น [ลักษณะการทำงานเริ่มต้น](electronic-reporting-destinations.md#default-behavior) สำหรับรูปแบบ ER ที่ไม่มีการตั้งค่าคอนฟิก [ปลายทาง](electronic-reporting-destinations.md) และที่กำลังทำงานในโหมดแบบโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="794d5-127">This behavior is the [default behavior](electronic-reporting-destinations.md#default-behavior) for an ER format that no [destinations](electronic-reporting-destinations.md) are configured for, and that is running in interactive mode.</span></span>

## <a name="review-the-source-code"></a><span data-ttu-id="794d5-128">ตรวจสอบโค้ดต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="794d5-128">Review the source code</span></span>

<span data-ttu-id="794d5-129">ทบทวนรหัสของวิธีการ `generateReportByGER()` ของคลาส `AssetRollForwardService`</span><span class="sxs-lookup"><span data-stu-id="794d5-129">Review the code of the `generateReportByGER()` method of the `AssetRollForwardService` class.</span></span> <span data-ttu-id="794d5-130">โปรดสังเกตว่า `Run()` มีการใช้วิธีการที่จะเรียกกรอบงาน ER และสร้างรายงาน **การกระทบยอดสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="794d5-130">Notice that the `Run()` method is used to call the ER framework and generate the **Fixed asset roll forward** report.</span></span>

```xpp
class AssetRollForwardService extends SysOperationServiceBase
{
    public const str ERFormatModelName = 'Fixed assets';
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'AssetRollForward';

    /// <summary>
    /// Generates report by general electronic reporting
    /// </summary>
    /// <param name = "_contract">The Asset Period Statement contract</param>
    public void generateReportByGER(AssetRollForwardContract _contract)
    {
        ERFormatMappingId   formatMappingId;
        AssetRollForwardDP  dataProvider;
        AssetRollForwardTmp assetRollForwardTmp;
        Query               query;

        query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
        dataProvider = AssetRollForwardDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

        if (assetRollForwardTmp)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                // Call ER to generate the report.
                ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName)
                    .withParameter(parameters)
                    .withFileDestination(_contract.getFileDestination())
                    .run();
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

## <a name="modify-the-source-code"></a><span data-ttu-id="794d5-131">ปรับเปลี่ยนโค้ดต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="794d5-131">Modify the source code</span></span>

1. <span data-ttu-id="794d5-132">ในโครงการของคุณ Visual Studio ให้เพิ่มคลาสใหม่ (`AssetRollForwardDestination` ในตัวอย่างนี้) และเขียนรหัสเพื่อใช้ปลายทางที่กำหนดเองของคุณสำหรับรายงาน **การกระทบยอดสินทรัพย์ถาวร** ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="794d5-132">In your Visual Studio project, add a new class (`AssetRollForwardDestination` in this example), and write code to implement your custom destination for **Fixed asset roll forward** reports that are generated.</span></span>

    - <span data-ttu-id="794d5-133">วิธีการ `new()` ได้รับการออกแบบมาเพื่อให้มีออบเจ็กต์ปลายทางของ ER ดั้งเดิมและพารามิเตอร์ที่ควบคุมโดยตรรกะของโปรแกรมประยุกต์ที่ระบุที่ตั้งที่กำหนดเองซึ่งควรจัดเก็บรายงานที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="794d5-133">The `new()` method is designed to get the original ER destination object and the application logic–driven parameter that specifies the custom location where generated reports should be stored.</span></span> <span data-ttu-id="794d5-134">ในตัวอย่างนี้ ที่ตั้งที่กำหนดเองคือชื่อของโฟลเดอร์ของระบบไฟล์ท้องถิ่นของเซิร์ฟเวอร์ที่รันบริการเซิร์ฟเวอร์โปรแกรมประยุกต์ออบเจ็กต์ (AOS)</span><span class="sxs-lookup"><span data-stu-id="794d5-134">In this example, the custom location is the name of a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    - <span data-ttu-id="794d5-135">วิธีการ `saveFile()` นี้ได้รับการออกแบบมาเพื่อบันทึกเอกสารที่สร้างขึ้นไปยังโฟลเดอร์ของระบบไฟล์ท้องถิ่นของเซิร์ฟเวอร์ที่รันบริการ AOS</span><span class="sxs-lookup"><span data-stu-id="794d5-135">The `saveFile()` method is designed to save a generated document to a folder of the local file system of the server that runs the AOS service.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    /// <summary>
    /// Destination class for <c>AssetRollForwardDestinationFactory</c> that stores a generated report.
    /// </summary>
    public class AssetRollForwardDestination implements ERIFileDestination
    {
        private ERIFileDestination originDestination;
        private str TargetFolder;

        /// <summary>
        /// Creates a stream for new file.
        /// </summary>
        /// <param name = "_fileName">Name of a new file.</param>
        /// <returns>Stream for new file.</returns>
        public System.IO.Stream newFileStream(System.String _fileName)
        {
            return originDestination.newFileStream(_fileName);
        }

        /// <summary>
        /// Saves file in destination.
        /// </summary>
        /// <param name = "_stream">A stream to save.</param>
        /// <param name = "_fileName">A file name.</param>
        /// <returns>Saved stream.</returns>
        public System.IO.Stream saveFile(System.IO.Stream _stream, System.String _fileName)
        {
            _stream.Seek(0, System.IO.SeekOrigin::Begin);
            using (var localStream = System.IO.File::OpenWrite(TargetFolder + _fileName))
            {
                _stream.CopyTo(localStream);
            }
            return _stream;
        }

        /// <summary>
        /// Constructs destination for fixed asset roll forward report.
        /// </summary>
        /// <param name = "_originDestination">The original destination.</param>
        /// <param name = "_TargetFoder">The folder to store a report that's being created.</param>
        /// <returns>The fixed asset roll forward destination.</returns>
        public static AssetRollForwardDestination construct(ERIFileDestination _originDestination, str _TargetFoder)
        {
            return new AssetRollForwardDestination(_originDestination, _TargetFoder);
        }

        protected void new(ERIFileDestination _originDestination, str _TargetFoder)
        {
            originDestination = _originDestination;
            TargetFolder = _TargetFoder;
        }
    }
    ```

2. <span data-ttu-id="794d5-136">ในโครงการ Visual Studio ของคุณ ให้เพิ่มคลาสใหม่ (`AssetRollForwardDestinationFactory` ในตัวอย่างนี้) และรหัสเขียนเพื่อตั้งค่าโรงงานปลายทางที่กำหนดเองซึ่งมอบสิทธิ์ในการสร้างปลายทางให้กับโรงงานปลายทางเริ่มต้น และตัดปลายทางไฟล์ด้วยปลายทางของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="794d5-136">In your Visual Studio project, add a new class (`AssetRollForwardDestinationFactory` in this example), and write code to set up a custom destination factory that delegates the creation of a destination to the default destination factory, and to wrap a file destination with your own destination.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using Microsoft.Dynamics365.LocalizationFramework.Format.FileGeneration;

    /// <summary>
    /// Destination factory for using <c>AssetRollForwardDestinationFactory</c>.
    /// </summary>
    public class AssetRollForwardDestinationFactory implements ERIFileDestinationFactory, ERIFileDestinationFactoryPostProcessor
    {
        private ERIFileDestinationFactory originDestinationFactory;
        private str TargetFolder;

        /// <summary>
        /// Creates file destination for print management.
        /// </summary>
        /// <param name = "_fileDestination">A default file destination.</param>
        /// <param name = "_identification">An identification strategy.</param>
        /// <param name = "_rootContext">A root context.</param>
        /// <param name = "_root">A root element.</param>
        /// <returns>A file destination.</returns>
        public ERIDataDrivenFileDestination createPrintMgmtDestination(
            ERIFileDestination _fileDestination,
            ERIObjectIdentificationStrategy _identification,
            ERTextFormatDataContext _rootContext,
            ERTextFormatIFileComponent _root)
        {
            ERIDataDrivenFileDestination dataDrivenDestination = originDestinationFactory.createPrintMgmtDestination(
                _fileDestination,
                _identification,
                _rootContext,
                _root);

            IFileDestinationHost fileDestinationHost = dataDrivenDestination as IFileDestinationHost;
            if (fileDestinationHost)
            {
                fileDestinationHost.FileDestination = AssetRollForwardDestination::construct(
                    fileDestinationHost.get_FileDestination(),
                    TargetFolder);
            }

            return dataDrivenDestination;
        }

        /// <summary>
        /// Constructs the fixed asset roll forward destination factory.
        /// </summary>
        /// <param name = "_originDestinationFactory">The original destination.</param>
        /// <param name = "_TargetFolder">The string containing a folder name that corresponds to the report, that's being created.</param>
        /// <returns>The destination factory for the fixed asset roll forward report.</returns>
        public static AssetRollForwardDestinationFactory construct(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            AssetRollForwardDestinationFactory destinationFactory = new AssetRollForwardDestinationFactory(_originDestinationFactory, _TargetFolder);

            ERIFileDestinationFactoryPostProcessorsHost factoryPostProcessing = ERCast::asObject(destinationFactory.originDestinationFactory) as ERIFileDestinationFactoryPostProcessorsHost;

            if (factoryPostProcessing)
            {
                factoryPostProcessing.addDestinationPostProcessor(destinationFactory);
            }
            return destinationFactory;
        }

        public ERIFileDestination processDestinationAfterCreation(ERIFileDestination _sourceDestination)
        {
            return AssetRollForwardDestination::construct(_sourceDestination, TargetFolder);
        }

        protected void new(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            originDestinationFactory = _originDestinationFactory;
            TargetFolder = _TargetFolder;
        }
    }
    ```

3. <span data-ttu-id="794d5-137">ปรับเปลี่ยนคลาส `AssetRollForwardService` ที่มีอยู่ และเขียนโค้ดเพื่อตั้งค่าโรงงานปลายทางที่กำหนดเองสำหรับผู้วิ่งรายงาน</span><span class="sxs-lookup"><span data-stu-id="794d5-137">Modify the existing `AssetRollForwardService` class, and write code to set up a custom destination factory for the report runner.</span></span> <span data-ttu-id="794d5-138">โปรดสังเกตว่าเมื่อมีการสร้างโรงงานปลายทางที่กำหนดเอง จะมีการส่งผ่านพารามิเตอร์ที่ใช้ในการควบคุมโปรแกรมประยุกต์ที่ระบุโฟลเดอร์เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="794d5-138">Notice that when a custom destination factory is constructed, the application-driven parameter that specifies a target folder is passed.</span></span> <span data-ttu-id="794d5-139">เมื่อต้องการจัดเก็บไฟล์ที่สร้างขึ้นในลักษณะนี้</span><span class="sxs-lookup"><span data-stu-id="794d5-139">In this way, that target folder is used to store generated files.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="794d5-140">ตรวจสอบให้แน่ใจว่าโฟลเดอร์ที่ระบุ (**c:\\0** ในตัวอย่างนี้) แสดงอยู่ในระบบไฟล์ท้องถิ่นของเซิร์ฟเวอร์ที่รันบริการ AOS</span><span class="sxs-lookup"><span data-stu-id="794d5-140">Make sure that the specified folder (**c:\\0** in this example) is present in the local file system of the server that runs the AOS service.</span></span> <span data-ttu-id="794d5-141">มิฉะนั้น ข้อยกเว้น [DirectoryNotFoundException](/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) จะเกิดขึ้นในขณะรันไทม์</span><span class="sxs-lookup"><span data-stu-id="794d5-141">Otherwise, a [DirectoryNotFoundException](/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) exception will be thrown at runtime.</span></span>

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    /// <summary>
    /// The electronic reporting service class for fixed asset roll forward report
    /// </summary>
    class AssetRollForwardService extends SysOperationServiceBase
    {
        public const str ERFormatModelName = 'Fixed assets';
        public const str ERModelDataSourceName = 'model';
        public const str DefaultExportedFileName = 'AssetRollForward';

        /// <summary>
        /// Generates report by general electronic reporting
        /// </summary>
        /// <param name = "_contract">The Asset Period Statement contract</param>
        public void generateReportByGER(AssetRollForwardContract _contract)
        {
            ERFormatMappingId   formatMappingId;
            AssetRollForwardDP  dataProvider;
            AssetRollForwardTmp assetRollForwardTmp;
            Query               query;

            query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
            dataProvider = AssetRollForwardDP::construct();
            formatMappingId = _contract.parmFormatMapping();
            assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

            if (assetRollForwardTmp)
            {
                try
                {
                    ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                        .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                        .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                    // Call ER to generate the report.
                    ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());

                    ERIFileDestinationFactoryHost factoryHost = ERCast::asObject(formatMappingRun) as ERIFileDestinationFactoryHost;
                    if (factoryHost)
                    {
                        ERIFileDestinationFactory fileDestinationFactory = factoryHost.getFileDestinationFactory();
                        factoryHost.setFileDestinationFactory(AssetRollForwardDestinationFactory::construct(fileDestinationFactory, @'c:\0\'));
                        formatMappingRun.run();
                    }
                }
                catch
                {
                    // An error occurred while exporting data.
                    error("@SYP4861341");
                }
            }
            else
            {
                // There is no data available.
                info("@SYS300117");
            }
        }
    }
    ```

4. <span data-ttu-id="794d5-142">สร้างโครงการของคุณใหม่</span><span class="sxs-lookup"><span data-stu-id="794d5-142">Rebuild your project.</span></span>

## <a name="re-run-the-fixed-asset-roll-forward-report"></a><span data-ttu-id="794d5-143">เรียกใช้รายงานการกระทบยอดสินทรัพย์ถาวรอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="794d5-143">Re-run the Fixed asset roll forward report</span></span>

1. <span data-ttu-id="794d5-144">ไปที่ **สินทรัพย์ถาวร** \> **การสอบถามและรายงาน** \> **รายงานธุรกรรม** \> **การกระทบยอดสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="794d5-144">Go to **Fixed assets** \> **Inquiries and reports** \> **Transaction reports** \> **Fixed asset roll forward**.</span></span>
2. <span data-ttu-id="794d5-145">ในฟิลด์ **จากวันที่** ให้ป้อน **1/1/2017**</span><span class="sxs-lookup"><span data-stu-id="794d5-145">In the **From date** field, enter **1/1/2017**.</span></span>
3. <span data-ttu-id="794d5-146">ในฟิลด์ **ถึงวันที่** ให้ป้อน **1/31/2017**</span><span class="sxs-lookup"><span data-stu-id="794d5-146">In the **To date** field, enter **1/31/2017**.</span></span>
4. <span data-ttu-id="794d5-147">ใน **ฟิลด์สกุลเงิน** ให้เลือก **สกุลเงินการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="794d5-147">In the **Currency field**, select **Accounting currency**.</span></span>
5. <span data-ttu-id="794d5-148">ในฟิลด์ **รูปแบบการแม็ป** ให้เลือก **การกระทบยอดสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="794d5-148">In the **Format mapping** field, select **Fixed asset roll forward**.</span></span>
6. <span data-ttu-id="794d5-149">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="794d5-149">Select **OK**.</span></span>
7. <span data-ttu-id="794d5-150">เลือกดูโฟลเดอร์ **c:\\0** ท้องถิ่น เพื่อค้นหาไฟล์ที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="794d5-150">Browse the local **C:\\0** folder to find the generated file.</span></span>

> [!NOTE]
> <span data-ttu-id="794d5-151">เนื่องจาก `originDestination` ไม่มีการใช้ออบเจ็กต์ในออบเจ็กต์ `AssetRollForwardDestination` ในตัวอย่างนี้ การตั้งค่าคอนฟิกสำหรับ [ปลายทาง](electronic-reporting-destinations.md) รูปแบบ ER จะถูกละเว้นเมื่อรันไทม์</span><span class="sxs-lookup"><span data-stu-id="794d5-151">Because the `originDestination` object isn't used in the `AssetRollForwardDestination` object in this example, the configurations for the ER format [destinations](electronic-reporting-destinations.md) will be ignored at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="794d5-152">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="794d5-152">Additional resources</span></span>

- [<span data-ttu-id="794d5-153">ปลายทางการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="794d5-153">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="794d5-154">หน้าแรกของความสามารถในการเพิ่มฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="794d5-154">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]