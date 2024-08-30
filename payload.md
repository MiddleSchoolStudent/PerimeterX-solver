### PX11307
n / a

### PX11309
```javascript
function gd(t, e) {
    try {
        if (t && t[e]) {
            var n = new t[e]("");
            var r = "";
            for (var a in n) if (n.hasOwnProperty(a)) {
            r += a;
            }
            return undefined ? undefined ? At(undefined, r) : Et(At(undefined, r)) : undefined ? Rt(r) : Et(Rt(r));
        }
    } catch (t) {}
    return "no_fp";
}

return gd(window, "WebKitCSSMatrix");
```

### PX11311
```javascript
function Wd(t) {
    if (Pd !== t) {
    (t ? zo : Jo)(document, "click", Gd);
    Pd = t;
    }
}

function zo(t, e, n, r) {
    try {
    var a;
    if (t && e && f(n) === "function" && f(e) === "string") {
        if (f(t.addEventListener) === "function") {
        if (Wo) {
            a = false;
            if (f(r) === "boolean") {
            a = r;
            } else if (r && f(r.useCapture) === "boolean") {
            a = r.useCapture;
            } else if (r && f(r.capture) === "boolean") {
            a = r.capture;
            }
        } else if (f(r) === "object" && null !== r) {
            a = {};
            if (r.hasOwnProperty("capture")) {
            a.capture = r.capture || false;
            }
            if (r.hasOwnProperty("once")) {
            a.once = r.once;
            }
            if (r.hasOwnProperty("passive")) {
            a.passive = r.passive;
            }
            if (r.hasOwnProperty("mozSystemGroup")) {
            a.mozSystemGroup = r.mozSystemGroup;
            }
        } else {
            a = {
            passive: true,
            capture: f(r) === "boolean" && r || false
            };
        }
        t.addEventListener(e, n, a);
        } else if (f(t.attachEvent) === "function") {
        t.attachEvent("on" + e, n);
        }
    }
    } catch (t) {}
}

function Jo(t, e, n) {
    try {
    if (t && e && f(n) === "function" && f(e) === "string") {
        if (f(t.removeEventListener) === "function") {
        t.removeEventListener(e, n);
        } else if (f(t.detachEvent) === "function") {
        t.detachEvent("on" + e, n);
        }
    }
    } catch (t) {}
}

function Wd(t) {
    if (Pd !== t) {
    (t ? zo : Jo)(document, "click", Gd);
    Pd = t;
    }
}

function Gd(t) {
    var e;
    if (Qd) {
    var r = function (t) {
        try {
        if (!t || !t.isTrusted) {
            return false;
        }
        var e = Io(t);
        if (!e) {
            return false;
        }
        var n = e.getClientRects();
        var r = {
            x: n[0].left + n[0].width / 2,
            y: n[0].top + n[0].height / 2
        };
        var a = Math.abs(r.x - t.clientX);
        var o = Math.abs(r.y - t.clientY);
        if (a < 1 && o < 1) {
            return {
            centerX: a,
            centerY: o
            };
        }
        } catch (t) {}
        return null;
    }(t);
    if (r) {
        Yd++;
        var a = Io(t);
        var o = Zo(a);
        var i = No(a);
        u(e = {}, "PX11652", o);
        u(e, "PX12305", r.centerX);
        u(e, "PX11311", r.centerY);
        u(e, "PX11427", i.top);
        u(e, "PX12208", i.left);
        u(e, "PX11824", a.offsetWidth);
        u(e, "PX11631", a.offsetHeight);
        u(e, "PX12129", Yd);
        lf("PX12030", e);
        if (5 <= Yd) {
        Qd = false;
        Wd(false);
        }
    }
    }
}

```

### PX11316
```javascript
{
    name: "PX11316",
    func: function () {
    return !!document.body.addBehavior;
    },
    defValue: false
}
```

### PX11325
n / a

### PX11339
```javascript
var Bv = function () {
    var e = new RegExp("/api/v2/collector", "g");
    return ft ? [new RegExp("/".concat(Gy[Me].replace("PX", ""), "/init.js"), "g"), e] : [/(?:https?:)?\/\/client(?:-stg)?\.(?:perimeterx\.net|a\.pxi\.pub|px-cdn\.net|px-cloud\.net)\/PX[A-Za-z0-9]{4,8}\/main\.min\.js/g, e];
};

var my = function () {
    var t = arguments.length > 0 && undefined !== arguments[0] ? arguments[0] : {};
    var e = t.regexList;
    var n = t.urlContainsList;
    var r = t.entriesFilter;
    var a = undefined === r ? function () {
    return true;
    } : r;
    if (!(f(or(window, "performance.getEntries", null)) === "function")) {
    return [];
    }
    var o = window.performance.getEntries().filter(a);
    var c = [];
    for (var i = 0; i < o.length; i++) {
    var u = o[i];
    if (e) {
        for (var s = 0; s < e.length; s++) {
        var h = e[s];
        if ("string" == typeof h) {
            h = new RegExp(e[s]);
        }
        if (h && f(h.test) === "function" && h.test(u.name)) {
            c.push(u);
        }
        }
    } else if (n) {
        for (var l = 0; l < n.length; l++) {
        var d = n[l];
        if (-1 !== u.name.indexOf(d)) {
            c.push(u);
        }
        }
    }
    }
    return c;
};

function gv() {
    if (Yn && Yn.hasOwnProperty(Fn[jt])) {
    try {
        var e = Bv();
        var n = my({
        regexList: [e[0]]
        })[0];
        if (n) {
        mv("PX11807", n.duration);
        }
        var r = my({
        regexList: [e[1]]
        })[0];
        if (r) {
        mv("PX11339", r.duration);
        mv("PX12298", r.domainLookupEnd - r.domainLookupStart);
        }
    } catch (t) {}
    }
}
```

### PX11344
```javascript
function Zo(t, e) {
    if (!(t && (t instanceof Element || f(t) === "object" && null !== t && 1 === t.nodeType))) {
    return "";
    }
    var n;
    var r = t[Eo];
    if (r) {
    return e ? Mo(r) : r;
    }
    try {
    n = function (t) {
        if (t.id) {
        return "#" + t.id;
        }
        var e;
        var n = "";
        for (var r = 0; r < 20; r++) {
        if (!(t && t instanceof Element)) {
            return n;
        }
        if ("html" === t.tagName.toLowerCase()) {
            return n;
        }
        if (t.id) {
            return "#" + t.id + n;
        }
        if (!((e = xo(t)) instanceof Element)) {
            return t.tagName + n;
        }
        if (Co(n = Oo(t, e) + n)) {
            return n;
        }
        t = e;
        n = ">" + n;
        }
    }(t);
    n = n.replace(/^>/, "");
    n = e ? Mo(n) : n;
    t[Eo] = n;
    } catch (t) {}
    return n || t.id || t.tagName || "";
}

function Vc(t, e, n) {
    var r;
    if (e) {
    u(r = {}, "PX11918", e || "");
    u(r, "PX12242", n || "");
    u(r, "PX11652", Zo(t, true));
    lc("PX11344", r);
    }
}
```

### PX11352
```javascript
try {
    r = t.createBuffer();
    t.bindBuffer(t.ARRAY_BUFFER, r);
    var u = new Float32Array([-.2, -.9, 0, .4, -.26, 0, 0, .732134444, 0]);
    t.bufferData(t.ARRAY_BUFFER, u, t.STATIC_DRAW);
    r.itemSize = 3;
    r.numItems = 3;
    a = t.createProgram();
    o = t.createShader(t.VERTEX_SHADER);
    t.shaderSource(o, "attribute vec2 attrVertex;varying vec2 varyinTexCoordinate;uniform vec2 uniformOffset;void main(){varyinTexCoordinate=attrVertex+uniformOffset;gl_Position=vec4(attrVertex,0,1);}");
    t.compileShader(o);
    i = t.createShader(t.FRAGMENT_SHADER);
    t.shaderSource(i, "precision mediump float;varying vec2 varyinTexCoordinate;void main() {gl_FragColor=vec4(varyinTexCoordinate,0,1);}");
    t.compileShader(i);
    t.attachShader(a, o);
    t.attachShader(a, i);
    t.linkProgram(a);
    t.useProgram(a);
    a.vertexPosAttrib = t.getAttribLocation(a, "attrVertex");
    a.offsetUniform = t.getUniformLocation(a, "uniformOffset");
    t.enableVertexAttribArray(a.vertexPosArray);
    t.vertexAttribPointer(a.vertexPosAttrib, r.itemSize, t.FLOAT, false, 0, 0);
    t.uniform2f(a.offsetUniform, 1, 1);
    t.drawArrays(t.TRIANGLE_STRIP, 0, r.numItems);
    e.canvasfp = null === t.canvas ? "no_fp" : undefined ? undefined ? At(undefined, t.canvas.toDataURL()) : Et(At(undefined, t.canvas.toDataURL())) : undefined ? Rt(t.canvas.toDataURL()) : Et(Rt(t.canvas.toDataURL()));
    e.extensions = t.getSupportedExtensions() || ["no_fp"];
} catch (t) {
    e.errors.push("PX11982");
}

r.PX11352 = n.canvasfp;
```

### PX11353
```javascript
function n(n) {
    if (e) {
        for (var a = 0; a < zc.length; a++) {
        var o = zc[a];
        document.removeEventListener(o, e[o]);
        }
        e = null;
        t("PX11353", n);
    }
}
```

### PX11362
```javascript
function ci(t) {
    var n = ["storeItem", "retrieveItem", "isNodeReachable_"];
    try {
    var r = Object.getOwnPropertyNames(document);
    for (var a = 0; a < r.length; a++) {
        try {
        var o = document[r[a]];
        var i = Object.getOwnPropertyNames(o.__proto__).toString();
        for (var u = 0; u < n.length && -1 !== i.indexOf(n[u]); u++) {
            if (u === n.length - 1) {
            t("PX11362");
            }
        }
        } catch (t) {}
    }
    } catch (t) {}
}
```

### PX11380
```javascript
t.PX11380 = screen && +screen.colorDepth || 0;
```

### PX11388
n / a

### PX11390
```javascript
t.PX11390 = function () {
    try {
    return new Date().getTimezoneOffset();
    } catch (t) {
    return 9999;
    }
}();
```

### PX11393
```javascript
if (t.type === "mousemove" && f(t.movementX) === "number" && f(t.movementY) === "number") {
    if (Nu.length < 10) {
        Nu.push(+t.movementX.toFixed(2) + "," + +t.movementY.toFixed(2) + "," + ((e || +new Date()) - (Ao || 0)));
    }
    if (Vu.length < 50) {
        Vu.push(Wu(t));
    }
}
u(n, "PX11393", Nu.join("|"));
```

### PX11405
n / a

### PX11427
```javascript
function No(t) {
    try {
    var e = Element.prototype.getBoundingClientRect.call(t);
    return {
        left: e.left,
        top: e.top
    };
    } catch (t) {
    return {
        left: -1,
        top: -1
    };
    }
}
n.PX11427 = f.top;
```

### PX11429
```javascript
function _c(t, e, n) {
    var r = t[e];
    if (r) {
    t[e] = function () {
        var e = f(Array.from) === "function" ? Array.from(arguments) : Array.prototype.slice.call(arguments);
        try {
        Oc(n, u({}, "PX11976", e));
        } catch (t) {}
        return r.apply(this, e);
    };
    }
}
_c(document, "getElementsByTagName", "PX11429");
```

### PX11433
```javascript
(function (t, e) {
    if (t.type === "mousemove" && f(t.movementX) === "number" && f(t.movementY) === "number") {
    if (Nu.length < 10) {
        Nu.push(+t.movementX.toFixed(2) + "," + +t.movementY.toFixed(2) + "," + ((e || +new Date()) - (Ao || 0)));
    }
    if (Vu.length < 50) {
        Vu.push(Wu(t));
    }
    } else if (t.type === "touchmove") {
    var n = $u(t);
    if (n && f(n.screenX) === "number" && f(n.screenY) === "number") {
        if (Cu.length < 10) {
        var r = f(Eu.previousTouchmove.screenX) === "number" ? n.screenX - Eu.previousTouchmove.screenX : 0;
        var a = f(Eu.previousTouchmove.screenY) === "number" ? n.screenY - Eu.previousTouchmove.screenY : 0;
        Eu.previousTouchmove.screenX = n.screenX;
        Eu.previousTouchmove.screenY = n.screenY;
        Cu.push(+r.toFixed(2) + "," + +a.toFixed(2) + "," + ((e || +new Date()) - (Ao || 0)));
        }
        if (_u.length < 50) {
        _u.push(Wu(t));
        }
    }
    }
})(t, n);
u(n, "PX11433", _u.length > 0 ? _t(_u) : undefined);
```

### PX11448
```javascript
{
    name: "PX11448",
    func: function () {
    return !!window.sessionStorage;
    },
    defValue: false
}
```

### PX11450
```javascript
function Oc(t, e) {
    var n = arguments.length > 2 && undefined !== arguments[2] && arguments[2];
    if (Ec < 200) {
    var a;
    var o = Ct(Kn());
    var i = o[o.length - 1] || {};
    var f = i[0] || "";
    var s = i[1] || "";
    if (!n && -1 !== f.indexOf(Fa)) {
        return;
    }
    Ec++;
    u(a = {}, "PX12343", t);
    u(a, "PX12240", Wt(bc, s));
    u(a, "PX11944", Wt(Dc, f));
    wc.push(ct(a, e));
    }
}
HTMLFormElement.prototype.submit = function () {
    var e = f(Array.from) === "function" ? Array.from(arguments) : Array.prototype.slice.call(arguments);
    try {
        Oc("PX11450", e);
    } catch (t) {}
    return r.apply(this, e);
};
```

### PX11452
```javascript
function Oh(t, e) {
    var o = "";
    for (var c = 0; c < e.length; c++) {
    try {
        var i = e[c];
        o += "" + t.hasOwnProperty(i);
    } catch (t) {
        o += t;
    }
    }
    return It(o);
}
var mo = ["closed", "devicePixelRatio", "getSelection", "locationbar", "scrollbars", "crypto", "caches", "speechSynthesis", "menubar", "personalbar", "toolbar", "Dump", "VRDispaly", "VRDisplayCapabilities", "VRDisplayEvent", "VREyeParameters", "VRFieldOfView", "VRFrameData", "VRPose", "VRStageParameters", "mozInnerScreenX", "mozInnerScreenY", "mozRTCIceCandidate", "mozRTCPeerConnection", "mozRTCSessionDescription", "webkitMediaStream", "webkitRTCPeerConnection", "webkitSpeechGrammar", "webkitSpeechGrammarList", "webkitSpeechRecognition", "webkitSpeechRecognitionError", "webkitSpeechRecognitionEvent", "webkitURL", "scheduler", "getDefaultComputedStyle", "Yandex", "yandexAPI", "Chrome", "Opera", "onrendersubtreeactivation", "scheduler", "onactivateinvisible", "onoverscroll", "onscrollend", "ondevicemotion", "ondeviceorientation", "onabsolutedeviceorientation", "ondeviceproximity", "onuserproximity", "ondevicelight", "onvrdisplayconnect", "onvrdisplaydisconnect", "onvrdisplayactivate", "onvrdisplaydeactivate", "onvrdisplaypresentchange", "ondragexit", "onloadend", "onshow", "onelementpainted", "onmozfullscreenchange", "Onmozfullscreenerror", "Onabort", "Onafterprint", "Onanimationend", "Onanimationiteration", "Onanimationstart", "Onappinstalled", "Onauxclick", "onbeforeinstallprompt", "onbeforeprint", "onbeforeunload", "onbeforexrselect", "onblur", "oncancel", "oncanplay", "oncanplaythrough", "onchange", "onclick", "onclose", "oncontextmenu", "oncuechange", "ondblclick", "ondevicemotion", "ondeviceorientation", "ondeviceorientationabsolute", "ondrag", "ondragend", "ondragenter", "ondragleave", "ondragover", "ondragstart", "ondrop", "ondurationchange", "onemptied", "onended", "onerror", "onfocus", "onformdata", "ongotpointercapture", "onhashchange", "oninput", "oninvalid", "onkeydown", "onkeypress", "onkeyup", "onlanguagechange", "onload", "onloadeddata", "onloadedmetadata", "onloadstart", "onlostpointercapture", "onmessage", "onmessageerror", "onmousedown", "onmouseenter", "onmouseleave", "onmousemove", "onmouseout", "onmouseover", "onmouseup", "onmousewheel", "onoffline", "ononline", "onpagehide", "onpageshow", "onpause", "onplay", "onplaying", "onpointercancel", "onpointerdown", "onpointerenter", "onpointerleave", "onpointermove", "onpointerout", "onpointerover", "onpointerrawupdate", "onpointerup", "onpopstate", "onprogress", "onratechange", "onrejectionhandled", "onreset", "onresize", "onscroll", "onsearch", "onseeked", "onseeking", "onselect", "onselectionchange", "onselectstart", "onstalled", "onstorage", "onsubmit", "onsuspend", "ontimeupdate", "ontoggle", "ontransitioncancel", "ontransitionend", "ontransitionrun", "ontransitionstart", "onunhandledrejection", "onunload", "onvolumechange", "onwaiting", "onwebkitanimationend", "onwebkitanimationiteration", "onwebkitanimationstart", "onwebkittransitionend", "onwheel", "Math"];
t.PX11452 = Oh(window, mo);
```

### PX11454
```javascript
function To() {
    var t = function () {
    var t = null;
    if (undefined !== document.hidden) {
        t = "";
    } else {
        var e = ["webkit", "moz", "ms", "o"];
        for (var n = 0; n < e.length; n++) {
        if (undefined !== document[e[n] + "Hidden"]) {
            t = e[n];
            break;
        }
        }
    }
    return t;
    }();
    return document[("" === t ? "v" : "V") + "isibilityState"];
}
u(n, "PX11454", To());
```

### PX11455
```javascript
r.PX11455 = n.unmaskedRenderer;
```

### PX11463
n / a

### PX11474
```javascript
setTimeout(function () {
    var n = "no_fp";
    try {
    var r = lh(650, 12);
    if (r) {
        var a = sh(r);
        n = "PX11982";
        if (a) {
        a.font = "8px sans-serif";
        var o = 1;
        for (var c = 128512; c < 128591; c++) {
            a.fillText(fo("0x" + c.toString(16)), 8 * o, 8);
            o++;
        }
        n = undefined ? undefined ? At(undefined, a.canvas.toDataURL()) : Et(At(undefined, a.canvas.toDataURL())) : undefined ? Rt(a.canvas.toDataURL()) : Et(Rt(a.canvas.toDataURL()));
        }
    } else {
        n = "PX12423";
    }
    } catch (e) {
    n = "PX11474";
    }
    e(u({}, "PX11927", n));
}, 1);
```

### PX11477
```javascript
try {
    var r;
    var a = 0;
    if (f(t.getChannelData) === "function") {
        for (var o = 4500; o < 5e3; o++) {
        var i = t.getChannelData(0);
        if (i) {
            a += Math.abs(i[o]);
        }
        }
    }
    var s = a.toString();
    var h = s && (undefined ? undefined ? At(undefined, s) : Et(At(undefined, s)) : undefined ? Rt(s) : Et(Rt(s)));
    u(r = {}, "PX11477", s);
    u(r, "PX12109", h);
    e(r);
    } catch (t) {
    var l;
    u(l = {}, "PX11477", "no_fp");
    u(l, "PX12109", "no_fp");
    e(l);
}
```

### PX11488
n / a

### PX11510
```javascript
Rc = true;
xc();
u(e = {}, "PX11949", wc);
u(e, "PX12436", bc);
u(e, "PX645", t);
u(e, "PX11585", Dc);
u(e, "PX12312", wc.length);
u(e, "PX11803", kc);
u(e, "PX12072", bo(Uc));
u(e, "PX12323", Tc);
if (t) {
    var a = Ct(Kn());
    var o = a[a.length - 1] || {};
    e.PX12240 = Wt(bc, o[1]);
    e.PX11944 = Wt(Dc, o[0]);
}
lc("PX11510", e);
```

### PX11528
```javascript
Lt(t, "PX11528", function () {
    return Tl(Object.getOwnPropertyDescriptor(HTMLDocument.prototype, "cookie").get);
}, "");
```

### PX11534
```javascript
r.PX11534 = n.shadingLangulageVersion;
```

### PX11536
```javascript
r.PX11536 = n.extensions;
```

### PX11538
```javascript
Lt(t, "PX11538", function () {
return history && f(history.length) === "number" && history.length || -1;
}, -1);
```

### PX11539
```javascript
Lt(t, "PX11539", function () {
    return Tl(window.console.log);
}, "");
```

### PX11540
```javascript
t.PX11540 = window.matchMedia && window.matchMedia("(pointer:fine)").matches;
```

### PX11544
n / a

### PX11547
```javascript
function Hd(t) {
    var n = function (t) {
    try {
        if (true || f(null) !== "function" || Yn && Yn.hasOwnProperty(Fn[ie])) {
        return;
        }
        return null(t, lf, function (t) {
        return pn(t, nn[pe]);
        }, Tt);
    } catch (t) {}
    }(t);
    t.PX12501 = ro();
    if (n && !function (t) {
    if (!(f(t) === "object" && null !== t)) {
        return true;
    }
    for (var e in t) if (t.hasOwnProperty(e) && undefined !== t[e]) {
        return false;
    }
    return true;
    }(n)) {
    t = ct(t, n);
    }
    $l("PX11547", t);
}
```

### PX11551
```javascript
{
    name: "PX11551",
    func: function () {
    return gd(window, "WebGLContextEvent");
    }
}
```

### PX11555
```javascript
var jt = function () {
    try {
        return window.performance && window.performance.memory;
    } catch (t) {}
    }();
    if (jt) {
    t.PX11529 = jt.usedJSHeapSize;
    t.PX11555 = jt.jsHeapSizeLimit;
    t.PX11833 = jt.totalJSHeapSize;
}
```

### PX11564
```javascript
t.PX11564 = window.orientation;
```

### PX11567
```javascript
r.PX11567 = n.webglRenderer;
```

### PX11583
```javascript
t.PX11583 = navigator.language;
```

### PX11585
```javascript
 u(e, "PX11585", Dc);
```

### PX11589
```javascript
u(e = {}, "PX11589", r);
```

### PX11590
```javascript
function lf(t, e) {
    e.PX11902 = af++;
    e.PX11560 = Bo() || +new Date();
    if (ff(t, e)) {
    cf.push({
        t: t,
        d: e,
        ts: new Date().getTime()
    });
    if (t === "PX11782") {
        Yu("PX11994");
        rf.trigger("PX11782");
    }
    } else {
    of.push({
        t: t,
        d: e,
        ts: new Date().getTime()
    });
    }
}

lf("PX11590", a);
```

### PX11595
```javascript
n.PX11892 = function (t) {
    var n = [];
    try {
        if (!t.clipboardData || !t.clipboardData.items) {
        return null;
        }
        for (var r = 0; r < t.clipboardData.items.length; r++) {
        var a;
        var o = t.clipboardData.items[r];
        u(a = {}, "PX11819", o.kind);
        u(a, "PX11595", o.type);
        n.push(a);
        }
    } catch (t) {}
    return n;
}(t);
```

### PX11606
```javascript
if (!navigator.permissions) {
    return void (Kr = "PX11606");
}
```

### PX11607
```javascript
function Tv(t) {
    var e;
    var r = +new Date();
    u(e = {}, "PX11589", r);
    u(e, "PX11868", r - Ca);
    !function (t) {
    if (Yn && Yn.hasOwnProperty(Fn[de])) {
        t.PX12611 = fv;
        t.PX12612 = sv;
    }
    }(e);
    if (window.performance && window.performance.timing) {
    e.PX11742 = window.performance.timing.domComplete;
    e.PX12244 = window.performance.timing.loadEventEnd;
    }
    var o = {
    captchaMaxAge: bi,
    captchaMaxStale: wi
    };
    var i = o.captchaMaxStale;
    var f = o.captchaMaxAge;
    if (null !== i) {
    e.PX12616 = f;
    }
    if (null !== f) {
    e.PX12617 = i;
    }
    var s = t[_e]();
    var h = s.clientXhrErrors;
    var l = s.clientHttpErrorStatuses;
    var y = s.clientRoutesLength;
    var v = s.fallbackStartIndex;
    var p = s.clientFailures;
    var m = s.sendActivitiesCount;
    var g = s.captchaFailures;
    var B = s.PXHCBootstrapTries;
    var H = s.PXHCFakeVerificationResponse;
    e.PX11979 = h;
    e.PX11511 = l;
    e.PX11403 = y;
    e.PX11675 = v;
    if (t[Ve] >= 1) {
    e.PX12445 = t[Ve];
    }
    e.PX11346 = window.performance && f(window.performance.now) === "function";
    e.PX11731 = p;
    e.PX11704 = m;
    if (g > 1) {
    e.PX11905 = g;
    }
    if (B > 1) {
    e.PX11661 = B;
    }
    if (H) {
    e.PX11442 = true;
    }
    if (Qi === "89d5fa8d-180f-44a1-8497-06b5de2302d4") {
    e.PX11470 = true;
    }
    e.PX11363 = Bf;
    if (Oa) {
    var D = cr(["/init.js", "/main.min.js"], "script");
    var b = D.resourceSize;
    var w = D.resourcePath;
    e.PX12122 = b;
    e.PX11501 = w;
    }
    var k = window._pxAction;
    if (k && "b" !== k) {
    e.PX12057 = k;
    e.PX645 = Yi;
    e.PX11416 = Ci;
    e.PX1070 = Pi;
    e.PX1076 = Vi;
    }
    return e;
}
lf("PX11607", Tv(t));
```

### PX11621
```javascript
t.PX11621 = navigator.deviceMemory;
```

### PX11627
```javascript
function _c(t, e, n) {
    var r = t[e];
    if (r) {
    t[e] = function () {
        var e = f(Array.from) === "function" ? Array.from(arguments) : Array.prototype.slice.call(arguments);
        try {
        Oc(n, u({}, "PX11976", e));
        } catch (t) {}
        return r.apply(this, e);
    };
    }
}
_c(document, "getElementsByClassName", "PX11627");
```

### PX11631
```javascript
function Xu(t, e) {
    var n;
    if (!t) {
    return null;
    }
    var a;
    u(n = {}, "PX12343", "DOMMouseScroll" === (a = t.type) ? Ro : a);
    u(n, "PX12270", _o(t));
    if (e) {
    var i = Io(t);
    if (i) {
        var f = No(i);
        n.PX11427 = f.top;
        n.PX12208 = f.left;
        n.PX11652 = function (t) {
        var e = Zo(t, true);
        return e ? function (t) {
            if (!Hu[t]) {
            Hu[t] = Du++;
            }
            return Du;
        }(e) : 0;
        }(i);
        n.PX11824 = i.offsetWidth;
        n.PX11631 = i.offsetHeight;
        n.PX12165 = function (t) {
        return "submit" === t.type ? t.type : t.nodeName ? t.nodeName.toLowerCase() : "";
        }(i);
    } else {
        n.PX11652 = 0;
    }
    }
    return n;
}
```

### PX11634
```javascript
var qc = ["webdriver", "cd_frame_id_"];
function pi(t, e) {
    var n = -1;
    for (var r = 0; r < e.length; r++) {
    var a = e[r];
    if (Element.prototype.getAttribute.call(t, a)) {
        n = r;
        break;
    }
    }
    return n;
}

function di(t) {
    var n = pi(document.documentElement, qc);
    if (-1 !== n) {
    t("PX11634", n);
    }
}
```

### PX11645
```javascript
var yu = location && location.href || "";
r.PX11645 = yu;
```

### PX11648
```javascript
var n = {
    t: "PX12167",
    d: u({}, "PX11648", true)
};
```

### PX11650
```javascript
function Lt(t, e, n, r) {
    var a;
    try {
    a = n();
    } catch (t) {}
    if (f(a) === "undefined") {
    a = f(r) === "undefined" ? "missing" : r;
    }
    t[e] = a;
    return a;
}

Lt(t, "PX11650", function () {
    return f(window.atob) === "function" && /\{\s*\[native code\]\s*\}/.test("" + window.atob);
}, false);
```

### PX11652
```javascript

if (!(xu[o] !== "mousemove" && xu[o] !== "touchmove")) {
    e(document.body, xu[o], Lu);
}

function Lu(t) {
    try {
    var n = +new Date();
    var r = n - Au;
    hu = t.type;
    (function (t, e) {
        if (t.type === "mousemove" && f(t.movementX) === "number" && f(t.movementY) === "number") {
        if (Nu.length < 10) {
            Nu.push(+t.movementX.toFixed(2) + "," + +t.movementY.toFixed(2) + "," + ((e || +new Date()) - (Ao || 0)));
        }
        if (Vu.length < 50) {
            Vu.push(Wu(t));
        }
        } else if (t.type === "touchmove") {
        var n = $u(t);
        if (n && f(n.screenX) === "number" && f(n.screenY) === "number") {
            if (Cu.length < 10) {
            var r = f(Eu.previousTouchmove.screenX) === "number" ? n.screenX - Eu.previousTouchmove.screenX : 0;
            var a = f(Eu.previousTouchmove.screenY) === "number" ? n.screenY - Eu.previousTouchmove.screenY : 0;
            Eu.previousTouchmove.screenX = n.screenX;
            Eu.previousTouchmove.screenY = n.screenY;
            Cu.push(+r.toFixed(2) + "," + +a.toFixed(2) + "," + ((e || +new Date()) - (Ao || 0)));
            }
            if (_u.length < 50) {
            _u.push(Wu(t));
            }
        }
        }
    })(t, n);
    if (r > 50) {
        var a;
        Au = n;
        var o = Gu(t);
        u(a = {}, "PX12108", o.pageX);
        u(a, "PX12414", o.pageY);
        u(a, "PX11699", (n || +new Date()) - (Ao || 0));
        if (null === Eu[hu]) {
        var s = Xu(t, false);
        s.coordination_start = [a];
        s.coordination_end = [];
        Eu[hu] = s;
        } else {
        var h = Eu[hu].coordination_start;
        if (h.length >= Ru[hu] / 2 && (h = Eu[hu].coordination_end).length >= Ru[hu] / 2) {
            h.shift();
        }
        h.push(a);
        }
    }
    } catch (t) {}
}

function Ed(t) {
    var e;
    if (wd && t) {
    var r = function (t) {
        var e = {};
        if (!t) {
        return e;
        }
        var n = t.touches || t.changedTouches;
        Fo(n ? t = n[0] : t, e);
        return e;
    }(t);
    u(e = {}, "PX12108", r.x);
    u(e, "PX12414", r.y);
    u(e, "PX11984", Kn());
    u(e, "PX12303", t.type || "");
    u(e, "PX11699", (undefined || +new Date()) - (Ao || 0));
    u(e, "PX11987", _o(t));
    u(e, "PX12461", Xo(t.target));
    u(e, "PX11652", Zo(Io(t)));
    lf("PX12123", e);
    Ti(true);
    wd = false;
    }
}
```

### PX11659
```javascript
oo1o1o: function (t, e, n) {
    var i = {};
    try {
        i.PX11762 = t;
        i.PX12076 = e;
        i.PX11953 = eval(n);
    } catch (t) {
        i.PX12056 = t + "";
    }
    lf("PX11659", i);
}
```

### PX11663
```javascript
return Tl(document.documentElement.dispatchEvent);
```

### PX11673
```javascript
if (a) {
    var o = function (t) {
    var e;
    var r = Kn();
    var a = Ct(r);
    if (a.length > 0) {
        var o;
        var i = a[a.length - 1];
        u(o = {}, "PX11984", r);
        u(o, "PX11652", t);
        u(o, "PX12240", i[1] || "");
        u(o, "PX11944", i[0] || "");
        e = o;
    } else {
        var f;
        u(f = {}, "PX11984", r);
        u(f, "PX11652", t);
        e = f;
    }
    return e;
    }(a);
    var i = Xo(n);
    if (f(i) !== "undefined") {
    o.PX12461 = i;
    }
    lf("PX11673", o);
    if (5 <= ++ny) {
    ay = false;
    iy(false);
    }
}
```

### PX11676
```javascript
_c(document, "querySelectorAll", "PX11676");
```

### PX11678
```javascript
t.PX11678 = function () {
    if (window.PointerEvent && "maxTouchPoints" in navigator) {
    if (navigator.maxTouchPoints > 0) {
        return true;
    }
    } else {
    if (window.matchMedia && window.matchMedia("(any-hover: none), (any-pointer: coarse)").matches) {
        return true;
    }
    if (window.TouchEvent || "ontouchstart" in window) {
        return true;
    }
    }
    return false;
}();
```

### PX11679
```javascript
u(n, "PX11679", document.body && document.body.offsetWidth + "x" + document.body.offsetHeight || "");
```

### PX11681
```javascript
```

### PX11685
```javascript
t.PX11681 = navigator.languages;
```

### PX11698
```javascript
(function (t, e) {
    if (t.type === "mousemove" && f(t.movementX) === "number" && f(t.movementY) === "number") {
    if (Nu.length < 10) {
        Nu.push(+t.movementX.toFixed(2) + "," + +t.movementY.toFixed(2) + "," + ((e || +new Date()) - (Ao || 0)));
    }
    if (Vu.length < 50) {
        Vu.push(Wu(t));
    }
    } else if (t.type === "touchmove") {
    var n = $u(t);
    if (n && f(n.screenX) === "number" && f(n.screenY) === "number") {
        if (Cu.length < 10) {
        var r = f(Eu.previousTouchmove.screenX) === "number" ? n.screenX - Eu.previousTouchmove.screenX : 0;
        var a = f(Eu.previousTouchmove.screenY) === "number" ? n.screenY - Eu.previousTouchmove.screenY : 0;
        Eu.previousTouchmove.screenX = n.screenX;
        Eu.previousTouchmove.screenY = n.screenY;
        Cu.push(+r.toFixed(2) + "," + +a.toFixed(2) + "," + ((e || +new Date()) - (Ao || 0)));
        }
        if (_u.length < 50) {
        _u.push(Wu(t));
        }
    }
    }
})(t, n);

function _t(t) {
    var e = [];
    for (var n = 0; n < t.length; n += 2) {
    e.push(t[n]);
    }
    return e;
}

u(n, "PX11698", Vu.length > 0 ? _t(Vu) : undefined);
```

### PX11699
```javascript
u(a, "PX11699", t[r].PX11699 - t[r - 1].PX11699);
```

### PX11702
```javascript
var a = function (t) {
    var e;
    var r = Kn();
    var a = Ct(r);
    if (a.length > 0) {
    var o;
    var i = a[a.length - 1];
    u(o = {}, "PX11984", r);
    u(o, "PX11652", t);
    u(o, "PX12240", i[1] || "");
    u(o, "PX11944", i[0] || "");
    e = o;
    } else {
    var f;
    u(f = {}, "PX11984", r);
    u(f, "PX11652", t);
    e = f;
    }
    return e;
}(r);
var o = Xo(n);
if (f(o) !== "undefined") {
    a.PX12461 = o;
}
lf("PX11702", a);
if (5 <= ++jd) {
    zd = false;
    qd(false);
}
```

### PX11719
```javascript
u(n = {}, "PX11719", true);
```

### PX11745
```javascript
```

### PX11747
```javascript
```

### PX11754
```javascript
```

### PX11771
```javascript
```

### PX11781
```javascript
```

### PX11782
```javascript
```

### PX11796
```javascript
```

### PX11802
```javascript
```

### PX11803
```javascript
```

### PX11805
```javascript
```

### PX11807
```javascript
```

### PX11811
```javascript
```

### PX11813
```javascript
```

### PX11814
```javascript
```

### PX11819
```javascript
```

### PX11824
```javascript
```

### PX11826
```javascript
```

### PX11840
```javascript
```

### PX11842
```javascript
```

### PX11843
```javascript
```

### PX11844
```javascript
```

### PX11849
```javascript
```

### PX11859
```javascript
```

### PX11866
```javascript
```

### PX11868
```javascript
```

### PX11875
```javascript
```

### PX11883
```javascript
```

### PX11891
```javascript
```

### PX11897
```javascript
```

### PX11898
```javascript
```

### PX11900
```javascript
```

### PX11909
```javascript
```

### PX11910
```javascript
```

### PX11913
```javascript
```

### PX11918
```javascript
```

### PX11921
```javascript
```

### PX11925
```javascript
```

### PX11927
```javascript
```

### PX11933
```javascript
```

### PX11934
```javascript
```

### PX11940
```javascript
```

### PX11944
```javascript
```

### PX11948
```javascript
```

### PX11949
```javascript
```

### PX11951
```javascript
```

### PX11959
```javascript
```

### PX11976
```javascript
```

### PX11978
```javascript
```

### PX11982
```javascript
```

### PX11984
```javascript
```

### PX11986
```javascript
```

### PX11987
```javascript
```

### PX11993
```javascript
```

### PX11994
```javascript
```

### PX12002
```javascript
```

### PX12003
```javascript
```

### PX12013
```javascript
```

### PX12015
```javascript
```

### PX12027
```javascript
```

### PX12030
```javascript
```

### PX12032
```javascript
```

### PX12037
```javascript
```

### PX12040
```javascript
```

### PX12051
```javascript
```

### PX12072
```javascript
```

### PX12073
```javascript
```

### PX12085
```javascript
```

### PX12092
```javascript
```

### PX12095
```javascript
```

### PX12099
```javascript
```

### PX12108
```javascript
```

### PX12109
```javascript
```

### PX12121
```javascript
```

### PX12123
```javascript
```

### PX12128
```javascript
```

### PX12129
```javascript
```

### PX12131
```javascript
```

### PX12132
```javascript
```

### PX12142
```javascript
```

### PX12149
```javascript
```

### PX12151
```javascript
```

### PX12155
```javascript
```

### PX12159
```javascript
```

### PX12160
```javascript
```

### PX12167
```javascript
```

### PX12170
```javascript
```

### PX12196
```javascript
```

### PX12203
```javascript
```

### PX12207
```javascript
```

### PX12208
```javascript
```

### PX12210
```javascript
```

### PX12228
```javascript
```

### PX12230
```javascript
```

### PX12236
```javascript
```

### PX12240
```javascript
```

### PX12242
```javascript
```

### PX12256
```javascript
```

### PX12264
```javascript
```

### PX12270
```javascript
```

### PX12271
```javascript
```

### PX12273
```javascript
```

### PX12288
```javascript
```

### PX12292
```javascript
```

### PX12298
```javascript
```

### PX12299
```javascript
```

### PX12303
```javascript
```

### PX12305
```javascript
```

### PX12312
```javascript
```

### PX12323
```javascript
```

### PX12331
```javascript
```

### PX12343
```javascript
```

### PX12347
```javascript
```

### PX12349
```javascript
```

### PX12352
```javascript
```

### PX12354
```javascript
```

### PX12362
```javascript
```

### PX12366
```javascript
```

### PX12387
```javascript
```

### PX12389
```javascript
```

### PX12401
```javascript
```

### PX12404
```javascript
```

### PX12414
```javascript
```

### PX12419
```javascript
```

### PX12423
```javascript
```

### PX12427
```javascript
```

### PX12429
```javascript
```

### PX12436
```javascript
```

### PX12439
```javascript
```

### PX12445
```javascript
```

### PX12446
```javascript
```

### PX12452
```javascript
```

### PX12456
```javascript
```

### PX12457
```javascript
```

### PX12458
```javascript
```

### PX12461
```javascript
```

### PX12464
```javascript
```

### PX12465
```javascript
```

### PX12469
```javascript
```

### PX12470
```javascript
```

### PX12483
```javascript
```

### PX12486
```javascript
```

### PX12492
```javascript
```

### PX12527
```javascript
```

### PX12540
```javascript
```

### PX12541
```javascript
```

### PX12542
```javascript
```

### PX12543
```javascript
```

### PX12570
```javascript
```

### PX12572
```javascript
```

### PX12586
```javascript
```

### PX12616
```javascript
```

### PX12617
```javascript
```

### PX12621
```javascript
```

### PX12635
```javascript
```

### PX561
```javascript
```

### PX645
```javascript
```