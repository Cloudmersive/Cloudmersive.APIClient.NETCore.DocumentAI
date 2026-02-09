# Cloudmersive.APIClient.NETCore.DocumentAI.Api.ExtractApi

All URIs are relative to *https://api.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ExtractAllFieldsAndTables**](ExtractApi.md#extractallfieldsandtables) | **POST** /document-ai/document/extract/all | Extract All Fields and Tables of Data from a Document using AI
[**ExtractBarcodes**](ExtractApi.md#extractbarcodes) | **POST** /document-ai/document/extract/barcodes | Extract Barcodes of from a Document using AI
[**ExtractClassification**](ExtractApi.md#extractclassification) | **POST** /document-ai/document/extract/classify | Extract Classification or Category from a Document using AI
[**ExtractClassificationAdvanced**](ExtractApi.md#extractclassificationadvanced) | **POST** /document-ai/document/extract/classify/advanced | Extract Classification or Category from a Document using Advanced AI
[**ExtractFields**](ExtractApi.md#extractfields) | **POST** /document-ai/document/extract/fields | Extract Field Values from a Document using AI
[**ExtractFieldsAdvanced**](ExtractApi.md#extractfieldsadvanced) | **POST** /document-ai/document/extract/fields/advanced | Extract Field Values from a Document using Advanced AI
[**ExtractSplit**](ExtractApi.md#extractsplit) | **POST** /document-ai/document/extract/split | Intelligently Split a Combined Document into Sub-Documents using AI
[**ExtractSummary**](ExtractApi.md#extractsummary) | **POST** /document-ai/document/extract/summary | Extract Summary from a Document using AI
[**ExtractTables**](ExtractApi.md#extracttables) | **POST** /document-ai/document/extract/tables | Extract Tables of Data from a Document using AI
[**ExtractText**](ExtractApi.md#extracttext) | **POST** /document-ai/document/extract/text | Extract Text from a Document using AI


<a name="extractallfieldsandtables"></a>
# **ExtractAllFieldsAndTables**
> ExtractFieldsAndTablesResponse ExtractAllFieldsAndTables (string recognitionMode = null, string preprocessing = null, System.IO.Stream inputFile = null)

Extract All Fields and Tables of Data from a Document using AI

Extract all Fields and Tables, comprised of rows and columns of data, from a document using AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumes 100 API calls per page.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DocumentAI.Api;
using Cloudmersive.APIClient.NETCore.DocumentAI.Client;
using Cloudmersive.APIClient.NETCore.DocumentAI.Model;

namespace Example
{
    public class ExtractAllFieldsAndTablesExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new ExtractApi();
            var recognitionMode = recognitionMode_example;  // string | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional) 
            var preprocessing = preprocessing_example;  // string | Optional: Set the level of image pre-processing to enhance accuracy.  Possible values are 'Auto' (default), 'Paged', and 'Compatability'.  Use 'Paged' to treat each page as a separate document for extraction (requires Advanced recognitionMode).  Default is Auto. (optional) 
            var inputFile = new System.IO.Stream(); // System.IO.Stream | Input document, or photos of a document, to extract data from (optional) 

            try
            {
                // Extract All Fields and Tables of Data from a Document using AI
                ExtractFieldsAndTablesResponse result = apiInstance.ExtractAllFieldsAndTables(recognitionMode, preprocessing, inputFile);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ExtractApi.ExtractAllFieldsAndTables: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognitionMode** | **string**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **preprocessing** | **string**| Optional: Set the level of image pre-processing to enhance accuracy.  Possible values are &#39;Auto&#39; (default), &#39;Paged&#39;, and &#39;Compatability&#39;.  Use &#39;Paged&#39; to treat each page as a separate document for extraction (requires Advanced recognitionMode).  Default is Auto. | [optional] 
 **inputFile** | **System.IO.Stream**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractFieldsAndTablesResponse**](ExtractFieldsAndTablesResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="extractbarcodes"></a>
# **ExtractBarcodes**
> ExtractBarcodesAiResponse ExtractBarcodes (string recognitionMode = null, System.IO.Stream inputFile = null)

Extract Barcodes of from a Document using AI

Extract all barcodes from a document using AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG, HEIC and WEBP.  Consumes 100 API calls per page.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DocumentAI.Api;
using Cloudmersive.APIClient.NETCore.DocumentAI.Client;
using Cloudmersive.APIClient.NETCore.DocumentAI.Model;

namespace Example
{
    public class ExtractBarcodesExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new ExtractApi();
            var recognitionMode = recognitionMode_example;  // string | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional) 
            var inputFile = new System.IO.Stream(); // System.IO.Stream | Input document, or photos of a document, to extract data from (optional) 

            try
            {
                // Extract Barcodes of from a Document using AI
                ExtractBarcodesAiResponse result = apiInstance.ExtractBarcodes(recognitionMode, inputFile);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ExtractApi.ExtractBarcodes: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognitionMode** | **string**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **inputFile** | **System.IO.Stream**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractBarcodesAiResponse**](ExtractBarcodesAiResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="extractclassification"></a>
# **ExtractClassification**
> DocumentClassificationResult ExtractClassification (string categories = null, string recognitionMode = null, System.IO.Stream inputFile = null)

Extract Classification or Category from a Document using AI

Extract Classification or Category (e.g. Invoice, Receipt, Tax Form, or Form 1040, Form 1040 EZ, etc.) from a document using AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumes 100 API calls per page.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DocumentAI.Api;
using Cloudmersive.APIClient.NETCore.DocumentAI.Client;
using Cloudmersive.APIClient.NETCore.DocumentAI.Model;

namespace Example
{
    public class ExtractClassificationExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new ExtractApi();
            var categories = categories_example;  // string | Desired classification to extract (optional) 
            var recognitionMode = recognitionMode_example;  // string | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional) 
            var inputFile = new System.IO.Stream(); // System.IO.Stream | Input document, or photos of a document, to extract data from (optional) 

            try
            {
                // Extract Classification or Category from a Document using AI
                DocumentClassificationResult result = apiInstance.ExtractClassification(categories, recognitionMode, inputFile);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ExtractApi.ExtractClassification: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **categories** | **string**| Desired classification to extract | [optional] 
 **recognitionMode** | **string**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **inputFile** | **System.IO.Stream**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**DocumentClassificationResult**](DocumentClassificationResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="extractclassificationadvanced"></a>
# **ExtractClassificationAdvanced**
> DocumentAdvancedClassificationResult ExtractClassificationAdvanced (string recognitionMode = null, AdvancedExtractClassificationRequest body = null)

Extract Classification or Category from a Document using Advanced AI

Extract Classification or Category (e.g. Invoice, Receipt, Tax Form, or Form 1040, Form 1040 EZ, etc.) from a document using Advanced AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumes 100 API calls per page.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DocumentAI.Api;
using Cloudmersive.APIClient.NETCore.DocumentAI.Client;
using Cloudmersive.APIClient.NETCore.DocumentAI.Model;

namespace Example
{
    public class ExtractClassificationAdvancedExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new ExtractApi();
            var recognitionMode = recognitionMode_example;  // string | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional) 
            var body = new AdvancedExtractClassificationRequest(); // AdvancedExtractClassificationRequest | Input request to perform the classification on (optional) 

            try
            {
                // Extract Classification or Category from a Document using Advanced AI
                DocumentAdvancedClassificationResult result = apiInstance.ExtractClassificationAdvanced(recognitionMode, body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ExtractApi.ExtractClassificationAdvanced: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognitionMode** | **string**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **body** | [**AdvancedExtractClassificationRequest**](AdvancedExtractClassificationRequest.md)| Input request to perform the classification on | [optional] 

### Return type

[**DocumentAdvancedClassificationResult**](DocumentAdvancedClassificationResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="extractfields"></a>
# **ExtractFields**
> ExtractFieldsResponse ExtractFields (string fieldNames = null, string recognitionMode = null, System.IO.Stream inputFile = null)

Extract Field Values from a Document using AI

Extract Field Values (e.g. Invoice Number, Invoice Date, Business Card Phone Number, etc.) from a document using AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumes 100 API calls per page.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DocumentAI.Api;
using Cloudmersive.APIClient.NETCore.DocumentAI.Client;
using Cloudmersive.APIClient.NETCore.DocumentAI.Model;

namespace Example
{
    public class ExtractFieldsExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new ExtractApi();
            var fieldNames = fieldNames_example;  // string | Desired fields to extract, comma separated (optional) 
            var recognitionMode = recognitionMode_example;  // string | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional) 
            var inputFile = new System.IO.Stream(); // System.IO.Stream | Input document, or photos of a document, to extract data from (optional) 

            try
            {
                // Extract Field Values from a Document using AI
                ExtractFieldsResponse result = apiInstance.ExtractFields(fieldNames, recognitionMode, inputFile);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ExtractApi.ExtractFields: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fieldNames** | **string**| Desired fields to extract, comma separated | [optional] 
 **recognitionMode** | **string**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **inputFile** | **System.IO.Stream**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractFieldsResponse**](ExtractFieldsResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="extractfieldsadvanced"></a>
# **ExtractFieldsAdvanced**
> ExtractFieldsAdvancedResponse ExtractFieldsAdvanced (string recognitionMode = null, AdvancedExtractFieldsRequest body = null)

Extract Field Values from a Document using Advanced AI

Extract Field Values (e.g. Invoice Number, Invoice Date, Business Card Phone Number, etc.) from a document using Advanced AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumes 100 API calls per page.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DocumentAI.Api;
using Cloudmersive.APIClient.NETCore.DocumentAI.Client;
using Cloudmersive.APIClient.NETCore.DocumentAI.Model;

namespace Example
{
    public class ExtractFieldsAdvancedExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new ExtractApi();
            var recognitionMode = recognitionMode_example;  // string | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional) 
            var body = new AdvancedExtractFieldsRequest(); // AdvancedExtractFieldsRequest | Input request, including document file as byte array, and information on which fields to extract (optional) 

            try
            {
                // Extract Field Values from a Document using Advanced AI
                ExtractFieldsAdvancedResponse result = apiInstance.ExtractFieldsAdvanced(recognitionMode, body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ExtractApi.ExtractFieldsAdvanced: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognitionMode** | **string**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **body** | [**AdvancedExtractFieldsRequest**](AdvancedExtractFieldsRequest.md)| Input request, including document file as byte array, and information on which fields to extract | [optional] 

### Return type

[**ExtractFieldsAdvancedResponse**](ExtractFieldsAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="extractsplit"></a>
# **ExtractSplit**
> SplitDocumentResponse ExtractSplit (string recognitionMode = null, System.IO.Stream inputFile = null)

Intelligently Split a Combined Document into Sub-Documents using AI

Analyzes a document containing multiple sub-documents (such as a scanned batch of ID cards, forms, or mixed documents) and intelligently splits it into separate sub-documents.  Uses AI to detect document boundaries based on visual content, headers, names, and document types.  Returns the page ranges and PDF bytes for each identified sub-document.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumes 100 API calls per page.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DocumentAI.Api;
using Cloudmersive.APIClient.NETCore.DocumentAI.Client;
using Cloudmersive.APIClient.NETCore.DocumentAI.Model;

namespace Example
{
    public class ExtractSplitExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new ExtractApi();
            var recognitionMode = recognitionMode_example;  // string | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional) 
            var inputFile = new System.IO.Stream(); // System.IO.Stream | Input document containing multiple sub-documents to split (optional) 

            try
            {
                // Intelligently Split a Combined Document into Sub-Documents using AI
                SplitDocumentResponse result = apiInstance.ExtractSplit(recognitionMode, inputFile);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ExtractApi.ExtractSplit: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognitionMode** | **string**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **inputFile** | **System.IO.Stream**| Input document containing multiple sub-documents to split | [optional] 

### Return type

[**SplitDocumentResponse**](SplitDocumentResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="extractsummary"></a>
# **ExtractSummary**
> SummarizeDocumentResponse ExtractSummary (string recognitionMode = null, string language = null, System.IO.Stream inputFile = null)

Extract Summary from a Document using AI

Creates a 1 paragraph summary of the input document using Artificial Intelligence.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumes 100 API calls per page.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DocumentAI.Api;
using Cloudmersive.APIClient.NETCore.DocumentAI.Client;
using Cloudmersive.APIClient.NETCore.DocumentAI.Model;

namespace Example
{
    public class ExtractSummaryExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new ExtractApi();
            var recognitionMode = recognitionMode_example;  // string | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional) 
            var language = language_example;  // string | Optional; Three-letter language code (ISO 639) for the summary.  Default is ENG.  Possible language codes are: AAR,ABK,ACE,ACH,ADA,ADY,AFA,AFH,AFR,AIN,AKA,AKK,ALB,ALE,ALG,ALT,AMH,ANG,ANP,APA,ARA,ARC,ARG,ARM,ARN,ARP,ART,ARW,ASM,AST,ATH,AUS,AVA,AVE,AWA,AYM,AZE,BAD,BAI,BAK,BAL,BAM,BAN,BAQ,BAS,BAT,BEJ,BEL,BEM,BEN,BER,BHO,BIH,BIK,BIN,BIS,BLA,BNT,BOD,BOS,BRA,BRE,BTK,BUA,BUG,BUL,BUR,BYN,CAD,CAI,CAR,CAT,CAU,CEB,CEL,CES,CHA,CHB,CHE,CHG,CHI,CHK,CHM,CHN,CHO,CHP,CHR,CHU,CHV,CHY,CMC,CNR,COP,COR,COS,CPE,CPF,CPP,CRE,CRH,CRP,CSB,CUS,CYM,CZE,DAK,DAN,DAR,DAY,DEL,DEN,DEU,DGR,DIN,DIV,DOI,DRA,DSB,DUA,DUM,DUT,DYU,DZO,EFI,EGY,EKA,ELL,ELX,ENG,ENM,EPO,EST,EUS,EWE,EWO,FAN,FAO,FAS,FAT,FIJ,FIL,FIN,FIU,FON,FRA,FRE,FRM,FRO,FRR,FRS,FRY,FUL,FUR,GAA,GAY,GBA,GEM,GEO,GER,GEZ,GIL,GLA,GLE,GLG,GLV,GMH,GOH,GON,GOR,GOT,GRB,GRC,GRE,GRN,GSW,GUJ,GWI,HAI,HAT,HAU,HAW,HEB,HER,HIL,HIM,HIN,HIT,HMN,HMO,HRV,HSB,HUN,HUP,HYE,IBA,IBO,ICE,IDO,III,IJO,IKU,ILE,ILO,INA,INC,IND,INE,INH,IPK,IRA,IRO,ISL,ITA,JAV,JBO,JPN,JPR,JRB,KAA,KAB,KAC,KAL,KAM,KAN,KAR,KAS,KAT,KAU,KAW,KAZ,KBD,KHA,KHI,KHM,KHO,KIK,KIN,KIR,KMB,KOK,KOM,KON,KOR,KOS,KPE,KRC,KRL,KRO,KRU,KUA,KUM,KUR,KUT,LAD,LAH,LAM,LAO,LAT,LAV,LEZ,LIM,LIN,LIT,LOL,LOZ,LTZ,LUA,LUB,LUG,LUI,LUN,LUO,LUS,MAC,MAD,MAG,MAH,MAI,MAK,MAL,MAN,MAO,MAP,MAR,MAS,MAY,MDF,MDR,MEN,MGA,MIC,MIN,MIS,MKD,MKH,MLG,MLT,MNC,MNI,MNO,MOH,MON,MOS,MRI,MSA,MUL,MUN,MUS,MWL,MWR,MYA,MYN,MYV,NAH,NAI,NAP,NAU,NAV,NBL,NDE,NDO,NDS,NEP,NEW,NIA,NIC,NIU,NLD,NNO,NOB,NOG,NON,NOR,NQO,NSO,NUB,NWC,NYA,NYM,NYN,NYO,NZI,OCI,OJI,ORI,ORM,OSA,OSS,OTA,OTO,PAA,PAG,PAL,PAM,PAN,PAP,PAU,PEO,PER,PHI,PHN,PLI,POL,PON,POR,PRA,PRO,PUS,QUE,RAJ,RAP,RAR,ROA,ROH,ROM,RON,RUM,RUN,RUP,RUS,SAD,SAG,SAH,SAI,SAL,SAM,SAN,SAS,SAT,SCN,SCO,SEL,SEM,SGA,SGN,SHN,SID,SIN,SIO,SIT,SLA,SLK,SLO,SLV,SMA,SME,SMI,SMJ,SMN,SMO,SMS,SNA,SND,SNK,SOG,SOM,SON,SOT,SPA,SQI,SRD,SRN,SRP,SRR,SSA,SSW,SUK,SUN,SUS,SUX,SWA,SWE,SYC,SYR,TAH,TAI,TAM,TAT,TEL,TEM,TER,TET,TGK,TGL,THA,TIB,TIG,TIR,TIV,TKL,TLH,TLI,TMH,TOG,TON,TPI,TSI,TSN,TSO,TUK,TUM,TUP,TUR,TUT,TVL,TWI,TYV,UDM,UGA,UIG,UKR,UMB,UND,URD,UZB,VAI,VEN,VIE,VOL,VOT,WAK,WAL,WAR,WAS,WEL,WEN,WLN,WOL,XAL,XHO,YAO,YAP,YID,YOR,YPK,ZAP,ZBL,ZEN,ZGH,ZHA,ZHO,ZND,ZUL,ZUN,ZXX,ZZA. (optional) 
            var inputFile = new System.IO.Stream(); // System.IO.Stream | Input document, or photos of a document, to extract data from (optional) 

            try
            {
                // Extract Summary from a Document using AI
                SummarizeDocumentResponse result = apiInstance.ExtractSummary(recognitionMode, language, inputFile);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ExtractApi.ExtractSummary: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognitionMode** | **string**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **language** | **string**| Optional; Three-letter language code (ISO 639) for the summary.  Default is ENG.  Possible language codes are: AAR,ABK,ACE,ACH,ADA,ADY,AFA,AFH,AFR,AIN,AKA,AKK,ALB,ALE,ALG,ALT,AMH,ANG,ANP,APA,ARA,ARC,ARG,ARM,ARN,ARP,ART,ARW,ASM,AST,ATH,AUS,AVA,AVE,AWA,AYM,AZE,BAD,BAI,BAK,BAL,BAM,BAN,BAQ,BAS,BAT,BEJ,BEL,BEM,BEN,BER,BHO,BIH,BIK,BIN,BIS,BLA,BNT,BOD,BOS,BRA,BRE,BTK,BUA,BUG,BUL,BUR,BYN,CAD,CAI,CAR,CAT,CAU,CEB,CEL,CES,CHA,CHB,CHE,CHG,CHI,CHK,CHM,CHN,CHO,CHP,CHR,CHU,CHV,CHY,CMC,CNR,COP,COR,COS,CPE,CPF,CPP,CRE,CRH,CRP,CSB,CUS,CYM,CZE,DAK,DAN,DAR,DAY,DEL,DEN,DEU,DGR,DIN,DIV,DOI,DRA,DSB,DUA,DUM,DUT,DYU,DZO,EFI,EGY,EKA,ELL,ELX,ENG,ENM,EPO,EST,EUS,EWE,EWO,FAN,FAO,FAS,FAT,FIJ,FIL,FIN,FIU,FON,FRA,FRE,FRM,FRO,FRR,FRS,FRY,FUL,FUR,GAA,GAY,GBA,GEM,GEO,GER,GEZ,GIL,GLA,GLE,GLG,GLV,GMH,GOH,GON,GOR,GOT,GRB,GRC,GRE,GRN,GSW,GUJ,GWI,HAI,HAT,HAU,HAW,HEB,HER,HIL,HIM,HIN,HIT,HMN,HMO,HRV,HSB,HUN,HUP,HYE,IBA,IBO,ICE,IDO,III,IJO,IKU,ILE,ILO,INA,INC,IND,INE,INH,IPK,IRA,IRO,ISL,ITA,JAV,JBO,JPN,JPR,JRB,KAA,KAB,KAC,KAL,KAM,KAN,KAR,KAS,KAT,KAU,KAW,KAZ,KBD,KHA,KHI,KHM,KHO,KIK,KIN,KIR,KMB,KOK,KOM,KON,KOR,KOS,KPE,KRC,KRL,KRO,KRU,KUA,KUM,KUR,KUT,LAD,LAH,LAM,LAO,LAT,LAV,LEZ,LIM,LIN,LIT,LOL,LOZ,LTZ,LUA,LUB,LUG,LUI,LUN,LUO,LUS,MAC,MAD,MAG,MAH,MAI,MAK,MAL,MAN,MAO,MAP,MAR,MAS,MAY,MDF,MDR,MEN,MGA,MIC,MIN,MIS,MKD,MKH,MLG,MLT,MNC,MNI,MNO,MOH,MON,MOS,MRI,MSA,MUL,MUN,MUS,MWL,MWR,MYA,MYN,MYV,NAH,NAI,NAP,NAU,NAV,NBL,NDE,NDO,NDS,NEP,NEW,NIA,NIC,NIU,NLD,NNO,NOB,NOG,NON,NOR,NQO,NSO,NUB,NWC,NYA,NYM,NYN,NYO,NZI,OCI,OJI,ORI,ORM,OSA,OSS,OTA,OTO,PAA,PAG,PAL,PAM,PAN,PAP,PAU,PEO,PER,PHI,PHN,PLI,POL,PON,POR,PRA,PRO,PUS,QUE,RAJ,RAP,RAR,ROA,ROH,ROM,RON,RUM,RUN,RUP,RUS,SAD,SAG,SAH,SAI,SAL,SAM,SAN,SAS,SAT,SCN,SCO,SEL,SEM,SGA,SGN,SHN,SID,SIN,SIO,SIT,SLA,SLK,SLO,SLV,SMA,SME,SMI,SMJ,SMN,SMO,SMS,SNA,SND,SNK,SOG,SOM,SON,SOT,SPA,SQI,SRD,SRN,SRP,SRR,SSA,SSW,SUK,SUN,SUS,SUX,SWA,SWE,SYC,SYR,TAH,TAI,TAM,TAT,TEL,TEM,TER,TET,TGK,TGL,THA,TIB,TIG,TIR,TIV,TKL,TLH,TLI,TMH,TOG,TON,TPI,TSI,TSN,TSO,TUK,TUM,TUP,TUR,TUT,TVL,TWI,TYV,UDM,UGA,UIG,UKR,UMB,UND,URD,UZB,VAI,VEN,VIE,VOL,VOT,WAK,WAL,WAR,WAS,WEL,WEN,WLN,WOL,XAL,XHO,YAO,YAP,YID,YOR,YPK,ZAP,ZBL,ZEN,ZGH,ZHA,ZHO,ZND,ZUL,ZUN,ZXX,ZZA. | [optional] 
 **inputFile** | **System.IO.Stream**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**SummarizeDocumentResponse**](SummarizeDocumentResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="extracttables"></a>
# **ExtractTables**
> ExtractTablesResponse ExtractTables (string recognitionMode = null, System.IO.Stream inputFile = null)

Extract Tables of Data from a Document using AI

Extract Tables, comprised of rows and columns of data, from a document using AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumeds 100 API calls per page.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DocumentAI.Api;
using Cloudmersive.APIClient.NETCore.DocumentAI.Client;
using Cloudmersive.APIClient.NETCore.DocumentAI.Model;

namespace Example
{
    public class ExtractTablesExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new ExtractApi();
            var recognitionMode = recognitionMode_example;  // string | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional) 
            var inputFile = new System.IO.Stream(); // System.IO.Stream | Input document, or photos of a document, to extract data from (optional) 

            try
            {
                // Extract Tables of Data from a Document using AI
                ExtractTablesResponse result = apiInstance.ExtractTables(recognitionMode, inputFile);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ExtractApi.ExtractTables: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognitionMode** | **string**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **inputFile** | **System.IO.Stream**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractTablesResponse**](ExtractTablesResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="extracttext"></a>
# **ExtractText**
> ExtractTextResponse ExtractText (string recognitionMode = null, System.IO.Stream inputFile = null)

Extract Text from a Document using AI

Extract raw text from a document using AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Supports a wide range of languages.  Consumes 100 API calls per page.

### Example
```csharp
using System;
using System.Diagnostics;
using Cloudmersive.APIClient.NETCore.DocumentAI.Api;
using Cloudmersive.APIClient.NETCore.DocumentAI.Client;
using Cloudmersive.APIClient.NETCore.DocumentAI.Model;

namespace Example
{
    public class ExtractTextExample
    {
        public void main()
        {
            // Configure API key authorization: Apikey
            Configuration.Default.AddApiKey("Apikey", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Apikey", "Bearer");

            var apiInstance = new ExtractApi();
            var recognitionMode = recognitionMode_example;  // string | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images.  Set to Deterministic to directly extract text from digital documents without using AI. (optional) 
            var inputFile = new System.IO.Stream(); // System.IO.Stream | Input document, or photos of a document, to extract data from (optional) 

            try
            {
                // Extract Text from a Document using AI
                ExtractTextResponse result = apiInstance.ExtractText(recognitionMode, inputFile);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling ExtractApi.ExtractText: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognitionMode** | **string**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images.  Set to Deterministic to directly extract text from digital documents without using AI. | [optional] 
 **inputFile** | **System.IO.Stream**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractTextResponse**](ExtractTextResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

