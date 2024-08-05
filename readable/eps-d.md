### The steps to de-obfuscate eps-d:
1. Paste `eps-d` into `https://obf-io.deobfuscate.io/`.
2. Paste the output code into Chrome's JavaScript console to get the values `Gm`, `kB`, `gs`.
3. Execute this code in https://astexplorer.net/ using `@baber/parser` + `babelv7` transform.
4. Use http://jsnice.org/ to make the code look better.


```javascript
export default function (babel) {
  const { types: t } = babel;
  const strs = {
    Gm: 'RegExpchangedTouchesreadPixelsfillcreateEventaudio/mpeg_phantom11pt ArialfillStyleHelveticaNeueTRIANGLE_STRIPSerifaabortMAX_VERTEX_UNIFORM_VECTORSHIGH_FLOATerroredAgControl.AgControlcreateShaderheadaudio/wav; codecs="1"randomparentElementPristinaLOW_FLOATheightuserAgenttype..HIGH_INTcontentWindowfunction f(j){var results=0;for(i=0;i<5;i++){results+=i;}if(j%2==0){results+=3;return results;}else{return result;}}availTopwebgl_hpluginsDOMContentLoadedfilteravailHeightsupportedEntryTypesappNameMonotypeCorsivaskippedLeelawadeebeginPathShell.UIHelpervideo/ogg; codecs="theora"webgl_cccanvasavailLeftfbufferDatamintouchend\\sFuturaBkBTtagNameRealVideo.RealVideo(tm) ActiveX Control (32-bit)screenYAudioSimHei__webdriver_script_funcstringifytoUpperCase::EdwardianScriptCenturyglobalCompositeOperationdocumentElement, JuiceITlinkProgramgetAttribLocationwebgl_dNetscapelastModifiedFLOATaih^_[a-zA-Z]serif]getAttributekeys18pt Arialrgb(0,255,255)__webdriver_script_fn__webdriver_unwrappedimplementationQuickTimeCheckObject.QuickTimeCheck.1SequentumtouchmovegetUniformLocationtimeStamp#069scriptMEDIUM_FLOATconsoleVENDORKokilaMTmouseoverptcompileShaderLOW_INTindexedDBperformanceselenium-evaluatewindowcpuClassmapmultiplyWMPlayer.OCXonbindexOfArrayLucidaSansPMingLiUeattrVertexGOTHAMMicrosoftUighur72pxMAX_VARYING_VECTORS applyGillSanssic__SENTRY__pushgetBatteryisPointInPathwebglopenDatabaseno Error.nameActiveXObjectAcroPDF.PDFpermissionsinnerHTMLsuffixesdebugappFRAGMENT_SHADERchromevideotopcauseprecision mediump float;varying vec2 varyinTexCoordinate;void main() {gl_FragColor=vec4(varyinTexCoordinate,0,1);}nowinnerWidthMAX_VERTEX_TEXTURE_IMAGE_UNITSDocumentTimelineZWAdobeFIFRAME',
    UU: 'SWCtl.SWCtlmousedownMeiryoUIgetImageDataWebGLRenderingContextpstopInternalMsxml2.DOMDocumentfillTextwebgl_iomouseupmsMaxTouchPointsfunctionBatangsrcsmaxTouchPoints#f60ginnerHeightcreateBufferaddBehavioriframeparseIntexternal{[nativecode]}ARRAY_BUFFERAparajitaMTfontseleniumidentifierwebgl_metastartalphabeticsetTimeoutaudio/ogg; codecs="vorbis"Humanst521BTVERTEX_SHADERorientationtouchstartundefinedMAX_VIEWPORT_DIMSgetShaderPrecisionFormatJSONMTExtrauseProgramaudio/aac;canvas_hstring cast failedPerformanceObserverObjectclearTimeoutUNMASKED_RENDERER_WEBGLvendor(^|[^SmallFontsclientYdblclickFunctionsubstringduckduckgoHaettenschweilermessagerttaudio/x-m4a;GREEN_BITSCalibriGishaMTscreenTEMPORARYdriverdevicePixelRatiowebdriverirgetContextAttributesrgb(255,0,255)WorkergetExtension_Selenium_IDE_RecorderTrident__proto__mousemoveJSON.stringify exceptionunknownavailWidthsorttestbodytouchcancelno Error.stackmouseenter]|$)',
    kB: "BitstreamVeraSansMonoVERSIONFranklinGothicbaseRemoveChild_e421bb29PDF.PdfCtrlEXT_texture_filter_anisotropiccallSeleniumgetpowDateALIASED_LINE_WIDTH_RANGEsrprotocolAvantGardeBkBTQuickTime.QuickTimetArialUnicodeMSdocumentinsertBefore_e421bb29ogactualBoundingBoxAscentaudiochildrensymbolbuniformOffsetUniversCE55MediumlanguageexceededontouchstartRealPlayerMAX_TEXTURE_SIZETDCCtl.TDCCtlouterHeightstop2dcontainersetMathproductSubenableVertexAttribArraytext[valuerangeMinloadTimeslanguagescallPhantomdataslice])[fillRectMsxml2.XMLHTTPinterrogateMinionProhardwareConcurrencymatchcalltiminginterrogationnoneoffsetUniformonucreateHTMLDocumentnumItemsAdodb.StreamSTENCIL_BITSVrindaRGBAtoLowerCasedumpStringatcreateElementSHADING_LANGUAGE_VERSIONdriver-evaluatenametoStringLetterGothicfromCharCoderepeat ;; vertexPosArrayshaderSourceLucidaBrightrgb(255,255,0)addEventListenerUNSIGNED_BYTEUint8ArrayRealPlayer.RealPlayer(tm) ActiveX Control (32-bit)product__selenium_unwrappedvertexAttribPointerUNMASKED_VENDOR_WEBGL__nightmaredrawArrays~getSupportedExtensionscanvas_dsubstrlocationprecisionactualBoundingBoxDescentuniform2fWEBKIT_EXT_texture_filter_anisotropicMSOutlookMAX_COMBINED_TEXTURE_IMAGE_UNITSfirstChildSegoeUILightnamedItemradiusXgetParameterstyleMAX_TEXTURE_IMAGE_UNITSitemgetTimezoneOffsetcontentDocumentBLUE_BITSmmmmmmmmllicanPlayType_seleniumClarendoncharCodeAtclosePathStaccato222BTBiomeMT$evenoddprototypergba(102, 204, 0, 0.7)TRAJANPROcreateElementNSsltmeasureTextlengthwebdriver-evaluateHighTowergetTimebindWebGL2RenderingContextcreateImageDatastring cast: BankGothicMdBTnavigationStartarcrefreshAVENIRLTProArabicTypesettingdescription,",
    gs: `RED_BITSgetOwnPropertyNamesPIabs<iframe srcdoc=1></iframe>MAX_CUBE_MAP_TEXTURE_SIZEwidthstringTouchEventbtoaforceselfSTATIC_DRAWSkype.DetectionSCRIPTfromnopemonospaceMacromediaFlashPaper.MacromediaFlashPaperloadbindBufferALPHA_BITSMarlettMSReferenceSpecialtyinlineattachShaderuncollectablegetContextLevenimMTquerySelectorcurrentTimeMAX_TEXTURE_MAX_ANISOTROPY_EXTtoDataURLMAX_VERTEX_ATTRIBSnavigatorscreenX__fxdriver_unwrappedFilebuildIDhistoryvideo/webm; codecs="vp8, vorbis"reese84interrogator[depth limit]removeChildDEPTH_BITSjavascript:rmocx.RealPlayer G2 Control.1[\\u0080-\\uFFFF]insertBeforeprop_ocanvas_fontsjoin__fxdriver_evaluateno Error.cause.pixelDepthactualBoundingBoxRightMOZ_EXT_texture_filter_anisotropic'experimental-webglcreateProgramMYRIADPROFloat32ArrayitemSizeclientXobjectMSMinchomouseoutenabledPluginputImageDatadisplayPERSISTENT__webdriver_evaluateSCRIPTINARENDERERHELVforEachrmocx.RealPlayer G2 Controlplatform;;;textBaselinesans-serifdivgetPrototypeOfradiusY-actualBoundingBoxLeftantialiasARNOPROconnectioncrreeseSkipExpirationCheckBauhaus93$1MEDIUM_INTappendChildMAX_FRAGMENT_UNIFORM_VECTORSctscalevisualViewportremoveEventListener__selenium_evaluatedeviceMemoryvideo/mp4; codecs="avc1.4D401E"canvas_ioano Error.messageImpactedattribute vec2 attrVertex;varying vec2 varyinTexCoordinate;uniform vec2 uniformOffset;void main(){varyinTexCoordinate=attrVertex+uniformOffset;gl_Position=vec4(attrVertex,0,1);}createAttributeparentNode__driver_unwrapped[\\ud800-\\udbff]$startInternaldata:image/webpScripting.DictionarycFuturaMdBTShockwaveFlash.ShockwaveFlashDevalVRXCtrl.DevalVRXCtrl.1filenamemimeTypesCenturyGothicstMAX_RENDERBUFFER_SIZE__driver_evaluateALIASED_POINT_SIZE_RANGEMicrosoft Internet ExplorerreplaceMSUIGothiccanvas_oCwm fjordbank glyphs vext quiz,stack]([^__webdriver_script_functionvertexPosAttribEUROSTILEAgencyFBouterWidthimage/webpwebgl_o;video/mp4; codecs="avc1.42E01E"rangeMaxrectmouseleaveWebAssemblygetOwnPropertyDescriptorWEBGL_debug_renderer_inforotationAngledoNotTrack`,
  };

  return {
    name: "ast-transform", // not required
    visitor: {
      CallExpression(path) {
        if (
          t.isMemberExpression(path.node.callee) &&
          t.isIdentifier(path.node.callee.object) &&
          Object.keys(strs).includes(path.node.callee.object.name) &&
          t.isIdentifier(path.node.callee.property, { name: "substr" })
        ) {
          path.replaceWith(
            t.stringLiteral(
              strs[path.node.callee.object.name].substr(
                path.node.arguments[0].value,
                path.node.arguments[1].value
              )
            )
          );
        }
      },
    },
  };
}
```