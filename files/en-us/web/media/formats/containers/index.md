---
title: Media container formats (file types)
slug: Web/Media/Formats/Containers
tags:
  - Audio
  - Containers
  - File
  - Filetypes
  - Guide
  - MIME Types
  - MIMETypes
  - Media
  - Video
  - formats
---
<div>{{QuickLinksWithSubpages("/en-US/docs/Web/Media")}}</div>

<p>The format of audio and video media files is defined in two parts (three if a file has both audio and video in it, of course): the audio and/or video codecs used and the media container format (or file type) used. <span class="seoSummary">In this guide, we'll look at the container formats used most commonly on the web, covering basics about their specifications as well as their benefits, limitations, and ideal use cases.</span></p>

<p><a href="/en-US/docs/Web/API/WebRTC_API">WebRTC</a> does not use a container at all. Instead, it streams the encoded audio and video tracks directly from one peer to another using {{domxref("MediaStreamTrack")}} objects to represent each track. See <a href="/en-US/docs/Web/Media/Formats/WebRTC_codecs">Codecs used by WebRTC</a> for information about codecs commonly used for making WebRTC calls, as well as browser compatibility information around codec support in WebRTC.</p>

<h2 id="Common_container_formats">Common container formats</h2>

<p>While there are a vast number of media container formats, the ones listed below are the ones you are most likely to encounter. Some support only audio while others support both audio and video. The MIME types and extensions for each are listed.The most commonly used containers for media on the web are probably MPEG-4 (MP4), QuickTime Movie (MOV), and the Wavefile Audio File Format (WAV). However, you may also encounter MP3, Ogg, WebM, AVI, and other formats. Not all of these are broadly supported by browsers, however; some combinations of container and codec are sometimes given their own file extensions and MIME types as a matter of convenience, or because of their ubiquity. For example, an Ogg file with only an Opus audio track is sometimes referred to as an Opus file, and might even have the extension <code>.opus</code>. But it's still actually just an Ogg file.</p>

<p>In other cases, a particular codec, stored in a certain container type, is so ubiquitous that the pairing is treated in a unique fashion. A good example of this is the MP3 audio file, which is in fact an MPEG-1 container with a single audio track encoded using MPEG-1 Audio Layer III encoding. These files use the <code>audio/mp3</code> MIME type and the <code>.mp3</code> extension, even though their containers are just MPEG.</p>

<h3 id="Index_of_media_container_formats_file_types">Index of media container formats (file types)</h3>

<p>To learn more about a specific container format, find it in this list and click through to the details, which include information about what the container is typically useful for, what codecs it supports, and which browsers support it, among other specifics.</p>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="row">Codec name (short)</th>
   <th scope="col">Full codec name</th>
   <th scope="col">Browser compatibility</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <th scope="row">{{anch("3GP")}}</th>
   <td>Third Generation Partnership</td>
   <td>Firefox for Android</td>
  </tr>
  <tr>
   <th scope="row">{{anch("ADTS")}}</th>
   <td>Audio Data Transport Stream</td>
   <td>
     <p>Firefox</p>
     <p>Available only if available on the underlying operating system's media framework.</p></td>
  </tr>
  <tr>
   <th scope="row">{{anch("FLAC")}}</th>
   <td>Free Lossless Audio Codec</td>
   <td>Chrome 56, Edge 16, Firefox 51, Safari 11</td>
  </tr>
  <tr>
   <th scope="row">{{anch("MPEGMPEG-2", "MPEG / MPEG-2")}}</th>
   <td>Moving Picture Experts Group (1 and 2)</td>
   <td>—</td>
  </tr>
  <tr>
   <th scope="row">{{anch("MPEG-4_MP4", "MPEG-4 (MP4)")}}</th>
   <td>Moving Picture Experts Group 4</td>
   <td>Chrome 3, Edge 12, Firefox, Internet Explorer 9, Opera 24, Safari 3.1</td>
  </tr>
  <tr>
   <th scope="row">{{anch("Ogg")}}</th>
   <td>Ogg</td>
   <td>
     <p>Chrome 3, Firefox 3.5, Edge 17 (desktop only), Internet Explorer 9, Opera 10.50</p>
     <p>Edge requires <a href="https://www.microsoft.com/store/productId/9N5TDP8VCMHS">Web Media Extensions</a> to be installed.</p>
   </td>
  </tr>
  <tr>
   <th scope="row">{{anch("QuickTime", "QuickTime (MOV)")}}</th>
   <td>Apple QuickTime movie</td>
   <td>Only older versions of Safari, plus other browsers that supported Apple's QuickTime plugin</td>
  </tr>
  <tr>
   <th scope="row">{{anch("WebM")}}</th>
   <td>Web Media</td>
   <td>
     <p>Chrome 6, Edge 17 (desktop only), Firefox 4, Opera 10.6, Safari (WebRTC only)</p>
     <p>Edge requires <a href="https://www.microsoft.com/store/productId/9N5TDP8VCMHS">Web Media Extensions</a> to be installed.</p>
   </td>
  </tr>
 </tbody>
</table>

<p>Unless otherwise specified, both mobile and desktop browser compatibility is implied if a browser is listed here. Support is also implied only for the container itself, not for any specific codecs.</p>

<h3 id="3GP">3GP</h3>

<p>The <strong>3GP</strong> or <strong>3GPP</strong> media container is used to encapsulate audio and/or video that is specifically intended for transmission over cellular networks for consumption on mobile devices. The format was designed for use on 3G mobile phones, but can still be used on more modern phones and networks. However, the improved bandwidth availability and increased data caps on most networks has reduced the need for the 3GP format. However, this format is still used for slower networks and for lower-performance phones.</p>

<p>This media container format is derived from the ISO Base Media File Format and MPEG-4, but is specifically streamlined for lower bandwidth scenarios.</p>

<table class="standard-table">
 <caption>Base 3GP media MIME types</caption>
 <thead>
  <tr>
   <th scope="col">Audio</th>
   <th scope="col">Video</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>audio/3gpp</code></td>
   <td><code>video/3gpp</code></td>
  </tr>
  <tr>
   <td><code>audio/3gpp2</code></td>
   <td><code>video/3gpp2</code></td>
  </tr>
  <tr>
   <td><code>audio/3gp2</code></td>
   <td><code>video/3gp2</code></td>
  </tr>
 </tbody>
</table>

<p>These MIME types are the fundamental types for the 3GP media container; other types may be used depending on the specific codec or codecs in use; in addition, you can <a href="/en-US/docs/Web/Media/Formats/codecs_parameter#iso-bmff">add the <code>codecs</code> parameter</a> to the MIME type string to indicate which codecs are used for the audio and/or video tracks, and to optionally provide details about the profile, level, and/or other codec configuration specifics.</p>

<table class="standard-table">
 <caption>Video codecs supported by 3GP</caption>
 <thead>
  <tr>
   <th rowspan="2" scope="row" style="vertical-align: bottom;">Codec</th>
   <th colspan="4" scope="col" style="text-align: center;">Browser support</th>
  </tr>
  <tr>
   <th scope="col">Chrome</th>
   <th scope="col">Edge</th>
   <th scope="col">Firefox</th>
   <th scope="col">Safari</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <th scope="row">AVC (H.264)</th>
   <td></td>
   <td></td>
   <td></td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">H.263</th>
   <td></td>
   <td></td>
   <td></td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">MPEG-4 Part 2 (MP4v-es)</th>
   <td></td>
   <td></td>
   <td></td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">VP8</th>
   <td></td>
   <td></td>
   <td></td>
   <td></td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>Audio codecs supported by 3GP</caption>
 <thead>
  <tr>
   <th rowspan="2" scope="row" style="vertical-align: bottom;">Codec</th>
   <th colspan="4" scope="col" style="text-align: center;">Browser support</th>
  </tr>
  <tr>
   <th scope="col">Chrome</th>
   <th scope="col">Edge</th>
   <th scope="col">Firefox</th>
   <th scope="col">Safari</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <th scope="row">AMR-NB</th>
   <td></td>
   <td></td>
   <td></td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">AMR-WB</th>
   <td></td>
   <td></td>
   <td></td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">AMR-WB+</th>
   <td></td>
   <td></td>
   <td></td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">AAC-LC</th>
   <td></td>
   <td></td>
   <td></td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">HE-AAC v1</th>
   <td></td>
   <td></td>
   <td></td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">HE-AAC v2</th>
   <td></td>
   <td></td>
   <td></td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">MP3</th>
   <td></td>
   <td></td>
   <td></td>
   <td></td>
  </tr>
 </tbody>
</table>

<h3 id="ADTS">ADTS</h3>

<p><strong>Audio Data Transport Stream</strong> (<strong>ADTS</strong>) is a container format specified by MPEG-4 Part 3 for audio data, intended to be used for streamed audio, such as for Internet radio. It is, essentially, an almost bare stream of AAC audio data, comprised of ADTS frames with a minimal header.</p>

<table class="standard-table">
 <caption>ADTS media MIME types</caption>
 <thead>
  <tr>
   <th scope="col">Audio</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>audio/aac</code></td>
  </tr>
  <tr>
   <td><code>audio/mpeg</code></td>
  </tr>
 </tbody>
</table>

<p>The MIME type used for ADTS depends on what kind of audio frames are contained within. If ADTS frames are used, the <code>audio/aac</code> MIME type should be used. If the audio frames are in MPEG-1/MPEG-2 Audio Layer I, II, or III format, the MIME type should be <code>audio/mpeg</code>.</p>

<table class="standard-table">
 <caption>Audio codecs supported by ADTS</caption>
 <thead>
  <tr>
   <th rowspan="2" scope="row" style="vertical-align: bottom;">Codec</th>
   <th colspan="4" scope="col" style="text-align: center;">Browser support</th>
  </tr>
  <tr>
   <th scope="col">Chrome</th>
   <th scope="col">Edge</th>
   <th scope="col">Firefox</th>
   <th scope="col">Safari</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <th scope="row">AAC</th>
   <td></td>
   <td></td>
   <td>Yes</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">MP3</th>
   <td></td>
   <td></td>
   <td>Yes</td>
   <td></td>
  </tr>
 </tbody>
</table>

<p>Firefox support for AAC relies upon the operating system's media infrastructure, so it is available as long as the OS supports it.</p>

<h3 id="FLAC">FLAC</h3>

<p>The <strong>Free Lossless Audio Codec</strong> (<strong>FLAC</strong>) is a lossless audio codec; there is also an associated simple container format, also called FLAC, that can contain this audio. The format is not encumbered by any patents, so its use is safe from interference. FLAC files can only contain FLAC audio data.</p>

<table class="standard-table">
 <caption>FLAC media MIME type</caption>
 <thead>
  <tr>
   <th scope="col">Audio</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>audio/flac</code></td>
  </tr>
  <tr>
   <td><code>audio/x-flac</code> (non-standard)</td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>Audio codecs supported by FLAC</caption>
 <thead>
  <tr>
   <th rowspan="2" scope="row" style="vertical-align: bottom;">Codec</th>
   <th colspan="4" scope="col" style="text-align: center;">Browser support</th>
  </tr>
  <tr>
   <th scope="col">Chrome</th>
   <th scope="col">Edge</th>
   <th scope="col">Firefox</th>
   <th scope="col">Safari</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <th scope="row">FLAC</th>
   <td></td>
   <td></td>
   <td>Yes</td>
   <td></td>
  </tr>
 </tbody>
</table>

<h3 id="MPEGMPEG-2">MPEG/MPEG-2</h3>

<p>The <strong>{{interwiki("wikipedia", "MPEG-1")}}</strong> and <strong>{{interwiki("wikipedia", "MPEG-2")}}</strong> file formats are essentially identical. Created by the Moving Picture Experts Group (MPEG), these formats are widely used in physical media, including as the format of the video on DVD media.</p>

<p>On the internet, perhaps the most common use of the MPEG file format is to contain {{interwiki("wikipedia", "MPEG-1", "Layer_III/MP3", "MPEG-1 Audio Layer 3")}} sound data; the resulting files are the wildly popular MP3 file used by digital music devices around the world. Otherwise, MPEG-1 and MPEG-2 are not widely used in Web content.</p>

<p>The main differences between MPEG-1 and MPEG-2 take place in the media data formats rather than the container format. MPEG-1 was introduced in 1992; MPEG-2 was introduced in 1996.</p>

<table class="standard-table">
 <caption>MPEG-1 and MPEG-2 media MIME types</caption>
 <thead>
  <tr>
   <th scope="col">Audio</th>
   <th scope="col">Video</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>audio/mpeg</code></td>
   <td><code>video/mpeg</code></td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>Video codecs supported by MPEG-1 and MPEG-2</caption>
 <thead>
  <tr>
   <th rowspan="2" scope="row" style="vertical-align: bottom;">Codec</th>
   <th colspan="4" scope="col" style="text-align: center;">Browser support</th>
  </tr>
  <tr>
   <th scope="col">Chrome</th>
   <th scope="col">Edge</th>
   <th scope="col">Firefox</th>
   <th scope="col">Safari</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <th scope="row">MPEG-1 Part 2</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">MPEG-2 Part 2</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>Audio codecs supported by MPEG-1 and MPEG-2</caption>
 <thead>
  <tr>
   <th rowspan="2" scope="row" style="vertical-align: bottom;">Codec</th>
   <th colspan="4" scope="col" style="text-align: center;">Browser support</th>
  </tr>
  <tr>
   <th scope="col">Chrome</th>
   <th scope="col">Edge</th>
   <th scope="col">Firefox</th>
   <th scope="col">Safari</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <th scope="row">MPEG-1 Audio Layer I</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">MPEG-1 Audio Layer II</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">MPEG-1 Audio Layer III (MP3)</th>
   <td></td>
   <td></td>
   <td>Yes</td>
   <td></td>
  </tr>
 </tbody>
</table>

<h3 id="MPEG-4_MP4">MPEG-4 (MP4)</h3>

<p><strong>{{interwiki("wikipedia", "MPEG-4")}}</strong> (<strong>MP4</strong>) is the latest version of the MPEG file format. There are two versions of the format, defined in parts 1 and 14 of the specification. MP4 is a popular container today, as it supports several of the most-used codecs and is broadly supported.</p>

<p>The original MPEG-4 Part 1 file format was introduced in 1999; the version 2 format, defined in Part 14, was added in 2003. The MP4 file format is derived from the {{interwiki("wikipedia", "ISO base media file format")}}, which is directly derived from the {{interwiki("wikipedia", "QuickTime file format")}} developed by <a href="https://www.apple.com/">Apple</a>.</p>

<p>When specifying the MPEG-4 media type (<code>audio/mp4</code> or <code>video/mp4</code>), you can <a href="/en-US/docs/Web/Media/Formats/codecs_parameter#iso-bmff">add the <code>codecs</code> parameter</a> to the MIME type string to indicate which codecs are used for the audio and/or video tracks, and to optionally provide details about the profile, level, and/or other codec configuration specifics.</p>

<table class="standard-table">
 <caption>Base MPEG-4 media MIME types</caption>
 <thead>
  <tr>
   <th scope="col">Audio</th>
   <th scope="col">Video</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>audio/mp4</code></td>
   <td><code>video/mp4</code></td>
  </tr>
 </tbody>
</table>

<p>These MIME types are the fundamental types for the MPEG-4 media container; other MIME types may be used depending on the specific codec or codecs in use within the container. In addition, you can <a href="/en-US/docs/Web/Media/Formats/codecs_parameter#iso-bmff">add the <code>codecs</code> parameter</a> to the MIME type string to indicate which codecs are used for the audio and/or video tracks, and to optionally provide details about the profile, level, and/or other codec configuration specifics.</p>

<table class="standard-table">
 <caption>Video codecs supported by MPEG-4</caption>
 <thead>
  <tr>
   <th rowspan="2" scope="row" style="vertical-align: bottom;">Codec</th>
   <th colspan="4" scope="col" style="text-align: center;">Browser support</th>
  </tr>
  <tr>
   <th scope="col">Chrome</th>
   <th scope="col">Edge</th>
   <th scope="col">Firefox</th>
   <th scope="col">Safari</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <th scope="row">AVC (H.264)</th>
   <td></td>
   <td></td>
   <td>
     <p>Yes</p>
     <p>Firefox support for H.264 relies upon the operating system's media infrastructure, so it is available as long as the OS supports it.</p>
   </td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">AV1</th>
   <td></td>
   <td></td>
   <td>
     <p>Yes</p>
     <p>Firefox support for AV1 is currently disabled by default; it can be enabled by setting the preference <code>media.av1.enabled</code> to <code>true</code>.</p>
   </td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">H.263</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">MPEG-4 Part 2 Visual</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">VP9</th>
   <td></td>
   <td></td>
   <td>Yes</td>
   <td></td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>Audio codecs supported by MPEG-4</caption>
 <thead>
  <tr>
   <th rowspan="2" scope="row" style="vertical-align: bottom;">Codec</th>
   <th colspan="4" scope="col" style="text-align: center;">Browser support</th>
  </tr>
  <tr>
   <th scope="col">Chrome</th>
   <th scope="col">Edge</th>
   <th scope="col">Firefox</th>
   <th scope="col">Safari</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <th scope="row">AAC</th>
   <td></td>
   <td></td>
   <td>
     <p>Yes</p>
     <p>Firefox support for H.264 relies upon the operating system's media infrastructure, so it is available as long as the OS supports it.</p>
   </td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">FLAC</th>
   <td></td>
   <td></td>
   <td>Yes</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">MPEG-1 Audio Layer III (MP3)</th>
   <td></td>
   <td></td>
   <td>Yes</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">Opus</th>
   <td></td>
   <td></td>
   <td>Yes</td>
   <td></td>
  </tr>
 </tbody>
</table>

<h3 id="Ogg">Ogg</h3>

<p>The <strong>{{interwiki("wikipedia", "Ogg")}}</strong> container format is a free and open format maintained by the <a href="https://www.xiph.org/">Xiph.org Foundation</a>. The Ogg framework also defines patent unencumbered media data formats, such as the Theora video codec and the Vorbis and Opus audio codecs. <a href="https://xiph.org/ogg/">Xiph.org documents about the Ogg format</a> are available on their web site.</p>

<p>While Ogg has been around for a long time, it has never gained the wide support needed to make it a good first choice for a media container. You are typically better off using WebM, though there are times when Ogg is useful to offer, such as when you wish to support older versions of Firefox and Chrome which don't yet support WebM. For example, Firefox 3.5 and 3.6 support Ogg, but not WebM.</p>

<p>You can get more information about Ogg and its codecs in the <a href="https://en.flossmanuals.net/ogg-theora/">Theora Cookbook</a>.</p>

<table class="standard-table">
 <caption>Base Ogg media MIME types</caption>
 <thead>
  <tr>
   <th scope="col">Audio</th>
   <th scope="col">Video</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>audio/ogg</code></td>
   <td><code>video/ogg</code></td>
  </tr>
 </tbody>
</table>

<p>The <code>application/ogg</code> MIME type can be used when you don't necessarily know whether the media contains audio or video. If at all possible, you should use one of the specific types, but fall back to <code>application/ogg</code> if you don't know the content format or formats.</p>

<p>You can also <a href="/en-US/docs/Web/Media/Formats/codecs_parameter#ogg">add the <code>codecs</code> parameter</a> to the MIME type string to indicate which codecs are used for the audio and/or video tracks, and to optionally further describe the track media formats.</p>

<table class="standard-table">
 <caption>Video codecs supported by Ogg</caption>
 <thead>
  <tr>
   <th rowspan="2" scope="row" style="vertical-align: bottom;">Codec</th>
   <th colspan="4" scope="col" style="text-align: center;">Browser support</th>
  </tr>
  <tr>
   <th scope="col">Chrome</th>
   <th scope="col">Edge</th>
   <th scope="col">Firefox</th>
   <th scope="col">Safari</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <th scope="row">Theora</th>
   <td></td>
   <td></td>
   <td>Yes</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">VP8</th>
   <td></td>
   <td></td>
   <td>Yes</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">VP9</th>
   <td></td>
   <td></td>
   <td>Yes</td>
   <td></td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>Audio codecs supported by Ogg</caption>
 <thead>
  <tr>
   <th rowspan="2" scope="row" style="vertical-align: bottom;">Codec</th>
   <th colspan="4" scope="col" style="text-align: center;">Browser support</th>
  </tr>
  <tr>
   <th scope="col">Chrome</th>
   <th scope="col">Edge</th>
   <th scope="col">Firefox</th>
   <th scope="col">Safari</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <th scope="row">FLAC</th>
   <td></td>
   <td></td>
   <td>Yes</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">Opus</th>
   <td></td>
   <td></td>
   <td>Yes</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">Vorbis</th>
   <td></td>
   <td></td>
   <td>Yes</td>
   <td></td>
  </tr>
 </tbody>
</table>

<h3 id="QuickTime">QuickTime</h3>

<p>The <strong>QuickTime</strong> file format (<strong>QTFF</strong>, <strong>QT</strong>, or <strong>MOV</strong>) was created by Apple for use by its media framework of the same name. The extension for these files, <code>.mov</code>, comes from the fact that the format was initially used for movies and was usually called the "QuickTime movie" format. While QTFF served as the basis for the MPEG-4 file format, there are differences and the two are not quite interchangeable.</p>

<p>QuickTime files support any sort of time-based data, including audio and video media, text tracks, and so forth. QuickTime files are primarily supported by macOS, but for a number of years, QuickTime for Windows was available to access them on Windows. However, QuickTime for Windows is no longer supported by Apple as of early 2016, and <em>should not be used</em>, as there are known security concerns. However, Windows Media Player now has integrated support for  QuickTime version 2.0 and earlier files; support for later versions of QuickTime requires third-party additions.</p>

<p>On Mac OS, the QuickTime framework not only supported QuickTime format movie files and codecs, but supported a vast array of popular and specialty audio and video codecs, as well as still image formats. Through QuickTime, Mac applications (including web browsers, through the QuickTime plugin or direct QuickTime integration) were able to read and write audio formats including AAC, AIFF, MP3, PCM, and Qualcomm PureVoice; and video formats including AVI, DV, Pixlet, ProRes, FLAC, Cinepak, 3GP, H.261 through H.265, MJPEG, MPEG-1 and MPEG-4 Part 2, Sorenson, and many more.</p>

<p>In addition, a number of third-party components are available for QuickTime, some of which add support for additional codecs.</p>

<p>Because QuickTime support is, for all intents and purposes, primarily available on Apple devices, it is no longer widely used on the internet. Apple itself generally now uses MP4 for video. In addition, the QuickTime framework has been deprecated on the Mac for some time, and is no longer available at all starting in macOS 10.15 Catalina.</p>

<table class="standard-table">
 <caption>Base QuickTime media MIME type</caption>
 <thead>
  <tr>
   <th scope="col">Video</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>video/quicktime</code></td>
  </tr>
 </tbody>
</table>

<p>The <code>video/quicktime</code> MIME type is the fundamental type for the QuickTime media container. It's worth noting that QuickTime (the media framework on Mac operating systems) supports a wide variety of containers and codecs, so it actually supports many other MIME types.</p>

<p>You can <a href="/en-US/docs/Web/Media/Formats/codecs_parameter#iso-bmff">add the <code>codecs</code> parameter</a> to the MIME type string to indicate which codecs are used for the audio and/or video tracks, and to optionally provide details about the profile, level, and/or other codec configuration specifics.</p>

<table class="standard-table">
 <caption>Video codecs supported by QuickTime</caption>
 <thead>
  <tr>
   <th rowspan="2" scope="row" style="vertical-align: bottom;">Codec</th>
   <th colspan="4" scope="col" style="text-align: center;">Browser support</th>
  </tr>
  <tr>
   <th scope="col">Chrome</th>
   <th scope="col">Edge</th>
   <th scope="col">Firefox</th>
   <th scope="col">Safari</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <th scope="row">AVC (H.264)</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">Cinepak</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">Component Video</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">DV</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">H.261</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">H.263</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">MPEG-2</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">MPEG-4 Part 2 Visual</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">Motion JPEG</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">Sorenson Video 2</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">Sorenson Video 3</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>Audio codecs supported by QuickTime</caption>
 <thead>
  <tr>
   <th rowspan="2" scope="row" style="vertical-align: bottom;">Codec</th>
   <th colspan="4" scope="col" style="text-align: center;">Browser support</th>
  </tr>
  <tr>
   <th scope="col">Chrome</th>
   <th scope="col">Edge</th>
   <th scope="col">Firefox</th>
   <th scope="col">Safari</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <th scope="row">AAC</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">ALaw 2:1</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">Apple Lossless (ALAC)</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">HE-AAC</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">MPEG-1 Audio Layer III (MP3)</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">Microsoft ADPCM</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">µ-Law 2:1 (u-Law)</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
 </tbody>
</table>

<h3 id="WAVE_WAV">WAVE (WAV)</h3>

<p>The <strong>Waveform Audio File Format</strong> (<strong>WAVE</strong>), usually referred to as WAV due to its filename extension being <code>.wav</code>, is a format developed by Microsoft and IBM to store audio bitstream data.</p>

<p>It is derived from the Resource Interchange File Format (RIFF), and as such is similar to other formats such as Apple's AIFF. The WAV codec registry can be found at {{RFC(2361)}}; however, because nearly all WAV files use linear PCM, support for the other codecs is sparse.</p>

<p>The WAVE format was first released in 1991.</p>

<table class="standard-table">
 <caption>WAVE media MIME types</caption>
 <thead>
  <tr>
   <th scope="col">Audio</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>audio/wave</code></td>
  </tr>
  <tr>
   <td><code>audio/wav</code></td>
  </tr>
  <tr>
   <td><code>audio/x-wav</code></td>
  </tr>
  <tr>
   <td><code>audio/x-pn-wav</code></td>
  </tr>
 </tbody>
</table>

<p>The <code>audio/wave</code> MIME type is the standard type, and is preferred; however, the others have been used by various products over the years and may be used as well in some environments. </p>

<table class="standard-table">
 <caption>Audio codecs supported by WAVE</caption>
 <thead>
  <tr>
   <th rowspan="2" scope="row" style="vertical-align: bottom;">Codec</th>
   <th colspan="4" scope="col" style="text-align: center;">Browser support</th>
  </tr>
  <tr>
   <th scope="col">Chrome</th>
   <th scope="col">Edge</th>
   <th scope="col">Firefox</th>
   <th scope="col">Safari</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <th scope="row">ADPCM (Adaptive Differential Pulse Code Modulation)</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">GSM 06.10</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">LPCM (Linear Pulse Code Modulation)</th>
   <td></td>
   <td></td>
   <td>Yes</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">MPEG-1 Audio Layer III (MP3)</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
  <tr>
   <th scope="row">µ-Law (u-Law)</th>
   <td></td>
   <td></td>
   <td>No</td>
   <td></td>
  </tr>
 </tbody>
</table>

<h3 id="WebM">WebM</h3>

<p><strong>{{interwiki("wikipedia", "WebM")}}</strong> (<strong>Web Media</strong>) is a format based on {{interwiki("wikipedia", "Matroska")}} which is designed specifically for use in modern web environments. It's based entirely on free and open technologies and primarily uses codecs that are in turn free and open, although some products support other codecs in WebM containers as well.</p>

<p>WebM was first introduced in 2010 and is now widely supported. Compliant implementations of WebM are required to support the VP8 and VP9 video codecs and the Theora and Opus audio codecs. The WebM container format and its required codecs are all available under open licenses. Any other codecs may require a license to use.</p>

<table class="standard-table">
 <caption>WebM media MIME types</caption>
 <thead>
  <tr>
   <th scope="col">Audio</th>
   <th scope="col">Video</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>audio/webm</code></td>
   <td><code>video/webm</code></td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>Video codecs supported by WebM</caption>
 <thead>
  <tr>
   <th rowspan="2" scope="row" style="vertical-align: bottom;">Codec</th>
   <th colspan="4" scope="col" style="text-align: center;">Browser support</th>
  </tr>
  <tr>
   <th scope="col">Chrome</th>
   <th scope="col">Edge</th>
   <th scope="col">Firefox</th>
   <th scope="col">Safari</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <th scope="row">AV1</th>
   <td>Yes</td>
   <td>Yes</td>
   <td>
     <p>Yes</p>
     <p>Firefox support for AV1 was added to macOS in Firefox 66; for Windows in Firefox 67; and Firefox 68 on Linux. Firefox for Android does not yet support AV1; the implementation in Firefox is designed to use a secure process, which is not supported yet in Android.</p>
   </td>
   <td>Yes</td>
  </tr>
  <tr>
   <th scope="row">VP8</th>
   <td>Yes</td>
   <td>Yes</td>
   <td>Yes</td>
   <td>Yes</td>
  </tr>
  <tr>
   <th scope="row">VP9</th>
   <td>Yes</td>
   <td>Yes</td>
   <td>Yes</td>
   <td>Yes</td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>Audio codecs supported by WebM</caption>
 <thead>
  <tr>
   <th rowspan="2" scope="row" style="vertical-align: bottom;">Codec</th>
   <th colspan="4" scope="col" style="text-align: center;">Browser support</th>
  </tr>
  <tr>
   <th scope="col">Chrome</th>
   <th scope="col">Edge</th>
   <th scope="col">Firefox</th>
   <th scope="col">Safari</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <th scope="row">Opus</th>
   <td>Yes</td>
   <td>Yes</td>
   <td>Yes</td>
   <td>Yes</td>
  </tr>
  <tr>
   <th scope="row">Vorbis</th>
   <td>Yes</td>
   <td>Yes</td>
   <td>Yes</td>
   <td>Yes</td>
  </tr>
 </tbody>
</table>

<h2 id="Choosing_the_right_container">Choosing the right container</h2>

<p>There are a few factors to consider when selecting the best container or containers to use for your media. The relative importance of each will depend on your needs, your license requirements, and the compatibility requirements of your target audience.</p>

<h3 id="Guidelines">Guidelines</h3>

<p>The best choice also depends on what you'll be doing with the media. Playing back media is a different thing than recording and/or editing it. If you're going to be manipulating the media data, using an uncompressed format can improve performance, while using a lossless compressed format at least prevents the accumulation of noise as compression artifacts are multiplied with each re-compression that occurs.</p>

<ul>
 <li>If your target audience is likely to include users on mobile, especially on lower-end devices or on slow networks, consider providing a version of your media in a 3GP container with appropriate compression.</li>
 <li>If you have any specific encoding requirements, make sure the container you choose supports the appropriate codecs.</li>
 <li>If you want your media to be in a non-proprietary, open format, consider using one of the open container formats such as FLAC (for audio) or WebM (for video).</li>
 <li>If for any reason you are only able to provide media in a single format, choose a format that's available on the broadest selection of devices and browsers, such as MP3 (for audio) or MP4 (for video and/or audio).</li>
 <li>If your media is audio-only, choosing an audio-only container format likely makes sense. Now that the patents have all expired, MP3 is a widely supported and good choice. WAVE is good but uncompressed, so be aware of that before using it for large audio samples. FLAC is a very good choice, due to its lossless compression, if the target browsers all support it.</li>
</ul>

<p>Unfortunately, neither of the relatively major lossless compression formats (FLAC and ALAC) are universally supported. FLAC is the more broadly supported of the two, but is not supported by macOS without additional software installed, and is not supported at all on iOS. If you need to offer lossless audio, you may need to provide both FLAC and ALAC to get close to universal compatibility.</p>

<h3 id="Container_selection_advice">Container selection advice</h3>

<p>The tables below offer suggested containers to use in various scenarios. These are just suggestions. Be sure to consider the needs of your application and your organization before selecting a container format.</p>

<h4 id="Audio-only_files">Audio-only files</h4>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">If you need...</th>
   <th scope="col">Consider using this container format</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>Compressed files for general-purpose playback</td>
   <td>MP3 (MPEG-1 Audio Layer III)</td>
  </tr>
  <tr>
   <td>Losslessly compressed files</td>
   <td>FLAC with ALAC fallback</td>
  </tr>
  <tr>
   <td>Uncompressed files</td>
   <td>WAV</td>
  </tr>
 </tbody>
</table>

<p>Now that MP3's patents have all expired, the choice of audio file format has become much easier to make. It's no longer necessary to choose between MP3's broad compatibility and the need to pay royalties when using it.</p>

<h4 id="Video_files">Video files</h4>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">If you need...</th>
   <th scope="col">Consider using this container format</th>
  </tr>
  <tr>
   <td>General purpose video, preferably in an open format</td>
   <td>WebM (ideally with MP4 fallback)</td>
  </tr>
  <tr>
   <td>General purpose video</td>
   <td>MP4 (ideally with WebM or Ogg fallback)</td>
  </tr>
  <tr>
   <td>High compression optimized for slow connections</td>
   <td>3GP (ideally with MP4 fallback)</td>
  </tr>
  <tr>
   <td>Compatibility with older devices/browsers</td>
   <td>QuickTime (ideally with AVI and/or MPEG-2 fallback)</td>
  </tr>
 </thead>
</table>

<p>These suggestions make a number of assumptions. You should carefully consider the options before making a final decision, especially if you have a lot of media that will need to be encoded.</p>

<h2 id="Maximizing_compatibility_with_multiple_containers">Maximizing compatibility with multiple containers</h2>

<p>To optimize compatibility, it's worth considering providing more than one version of media files, using the {{HTMLElement("source")}} element to specify each source within the {{HTMLElement("audio")}} or {{HTMLElement("video")}} element. For example, you can offer an Ogg or WebM video as the first choice, with a fallback in MP4 format. You could even choose to offer a retro-like QuickTime or AVI fallback for good measure.</p>

<p>To do this, you create a <code>&lt;video&gt;</code> (or <code>&lt;audio&gt;</code>) element with no {{htmlattrxref("src", "video")}} attribute. Then add child {{HTMLElement("source")}} elements within the <code>&lt;video&gt;</code> element, one for each version of the video you offer. This can be used to offer various versions of a video that can be selected depending on bandwidth availability, but in our case, we'll use it to offer format options.</p>

<p>In the example shown here, a video is offered to the browser in two formats: WebM and MP4.</p>

<div>{{EmbedInteractiveExample("pages/tabbed/source.html", "tabbed-standard")}}</div>

<p>The video is offered first in WebM format (with the {{htmlattrxref("type", "video")}} attribute set to <code>video/webm</code>). If the {{Glossary("user agent")}} can't play that, it moves on to the next option, whose <code>type</code> is specified as <code>video/mp4</code>. If neither of those can be played, the text "This browser does not support the HTML5 video element." is presented.</p>

<h2 id="Specifications">Specifications</h2>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">Specification</th>
   <th scope="col">Comment</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><a href="https://portal.3gpp.org/desktopmodules/Specifications/SpecificationDetails.aspx?specificationId=1441">ETSI 3GPP</a></td>
   <td>Defines the 3GP container format</td>
  </tr>
  <tr>
   <td><a href="https://www.iso.org/standard/53943.html">ISO/IEC 14496-3</a> (MPEG-4 Part 3 Audio)</td>
   <td>Defines MP4 audio including ADTS</td>
  </tr>
  <tr>
   <td><a href="https://xiph.org/flac/format.html">FLAC Format</a></td>
   <td>The FLAC format specification</td>
  </tr>
  <tr>
   <td><a href="https://www.iso.org/standard/19180.html">ISO/IEC 11172-1</a> (MPEG-1 Part 1 Systems)</td>
   <td>Defines the MPEG-1 container format</td>
  </tr>
  <tr>
   <td><a href="https://www.iso.org/standard/74427.html">ISO/IEC 13818-1</a> (MPEG-2 Part 1 Systems)</td>
   <td>Defines the MPEG-2 container format</td>
  </tr>
  <tr>
   <td><a href="https://www.iso.org/standard/75929.html">ISO/IEC 14496-14</a> (MPEG-4 Part 14: MP4 file format)</td>
   <td>Defines the MPEG-4 (MP4) version 2 container format</td>
  </tr>
  <tr>
   <td><a href="https://www.iso.org/standard/55688.html">ISO/IEC 14496-1</a> (MPEG-4 Part 1 Systems)</td>
   <td>Defines the original MPEG-4 (MP4) container format</td>
  </tr>
  <tr>
   <td>{{RFC(3533)}}</td>
   <td>Defines the Ogg container format</td>
  </tr>
  <tr>
   <td>{{RFC(5334)}}</td>
   <td>Defines the Ogg media types and file extensions</td>
  </tr>
  <tr>
   <td><a href="https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html">QuickTime File Format Specification</a></td>
   <td>Defines the QuickTime movie (MOV) format</td>
  </tr>
  <tr>
   <td><a href="https://web.archive.org/web/20090417165828/http://www.kk.iij4u.or.jp/~kondo/wave/mpidata.txt">Multimedia Programming Interface and Data Specifications 1.0</a></td>
   <td>The closest thing to an official WAVE specification</td>
  </tr>
  <tr>
   <td><a href="https://docs.microsoft.com/en-us/windows/desktop/xaudio2/resource-interchange-file-format--riff-">Resource Interchange File Format</a> (used by WAV)</td>
   <td>Defines the RIFF format; WAVE files are a form of RIFF</td>
  </tr>
  <tr>
   <td><a href="https://www.webmproject.org/docs/container/">WebM Container Guidelines</a></td>
   <td>Guide for adapting Matroska for WebM</td>
  </tr>
  <tr>
   <td><a href="https://matroska.org/technical/specs/index.html">Matroska Specifications</a></td>
   <td>The specification for the Matroska container format upon which WebM is based</td>
  </tr>
  <tr>
   <td><a href="https://w3c.github.io/media-source/webm-byte-stream-format.html">WebM Byte Stream Format</a></td>
   <td>WebM byte stream format for use with <a href="/en-US/docs/Web/API/Media_Source_Extensions_API">Media Source Extensions</a></td>
  </tr>
 </tbody>
</table>

<h2 id="Browser_compatibility">Browser compatibility</h2>

<table class="standard-table">
 <thead>
  <tr>
   <th rowspan="2" scope="row" style="vertical-align: bottom;">Container format name</th>
   <th colspan="3" scope="col" style="text-align: center; border-right: 2px solid #d4dde4;">Audio</th>
   <th colspan="3" scope="col" style="text-align: center;">Video</th>
  </tr>
  <tr>
   <th scope="col" style="vertical-align: bottom;">MIME type</th>
   <th scope="col" style="vertical-align: bottom;">Extension(s)</th>
   <th scope="col" style="vertical-align: bottom; border-right: 2px solid #d4dde4;">Browser support</th>
   <th scope="col" style="vertical-align: bottom;">MIME type</th>
   <th scope="col" style="vertical-align: bottom;">Extension(s)</th>
   <th scope="col" style="vertical-align: bottom; border-right: 2px solid #d4dde4;">Browser support</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <th scope="row" style="vertical-align: bottom;">3GP</th>
   <td style="vertical-align: top;"><code>audio/3gpp</code></td>
   <td style="vertical-align: top;"><code>.3gp</code></td>
   <td style="vertical-align: top; border-right: 2px solid #d4dde4;">Firefox</td>
   <td style="vertical-align: top;"><code>video/3gpp</code></td>
   <td style="vertical-align: top;"><code>.3gp</code></td>
   <td style="vertical-align: top;">Firefox</td>
  </tr>
  <tr>
   <th scope="row" style="vertical-align: top;">ADTS (Audio Data Transport Stream)</th>
   <td style="vertical-align: top;"><code>audio/aac</code></td>
   <td style="vertical-align: top;"><code>.aac</code></td>
   <td style="vertical-align: top; border-right: 2px solid #d4dde4;">Firefox</td>
   <td style="vertical-align: top;">—</td>
   <td style="vertical-align: top;">—</td>
   <td style="vertical-align: top;">—</td>
  </tr>
  <tr>
   <th scope="row" style="vertical-align: top;">FLAC</th>
   <td style="vertical-align: top;"><code>audio/flac</code></td>
   <td style="vertical-align: top;"><code>.flac</code></td>
   <td style="vertical-align: top; border-right: 2px solid #d4dde4;">Firefox</td>
   <td style="vertical-align: top;">—</td>
   <td style="vertical-align: top;">—</td>
   <td style="vertical-align: top;">—</td>
  </tr>
  <tr>
   <th rowspan="2" scope="row" style="vertical-align: top;">MPEG-1 / MPEG-2 (MPG or MPEG)</th>
   <td style="vertical-align: top;"><code>audio/mpeg</code></td>
   <td style="vertical-align: top;"><code>.mpg</code><br>
    <code>.mpeg</code></td>
   <td style="vertical-align: top; border-right: 2px solid #d4dde4;">Firefox</td>
   <td rowspan="2" style="vertical-align: top;"><code>video/mpeg</code></td>
   <td rowspan="2" style="vertical-align: top;"><code>.mpg</code><br>
    <code>.mpeg</code></td>
   <td rowspan="2" style="vertical-align: top;">Firefox</td>
  </tr>
  <tr>
   <td style="vertical-align: top;"><code>audio/mp3</code></td>
   <td style="vertical-align: top;"><code>.mp3</code></td>
   <td style="vertical-align: top; border-right: 2px solid #d4dde4;">Firefox</td>
  </tr>
  <tr>
   <th scope="row" style="vertical-align: top;">MPEG-4 (MP4)</th>
   <td style="vertical-align: top;"><code>audio/mp4</code></td>
   <td style="vertical-align: top;"><code>.mp4</code><br>
    <code>.m4a</code></td>
   <td style="vertical-align: top; border-right: 2px solid #d4dde4;">Firefox</td>
   <td style="vertical-align: top;"><code>video/mp4</code></td>
   <td style="vertical-align: top;"><code>.mp4</code><br>
    <code>.m4v</code><br>
    <code>.m4p</code></td>
   <td style="vertical-align: top;">Firefox</td>
  </tr>
  <tr>
   <th scope="row" style="vertical-align: top;">Ogg</th>
   <td style="vertical-align: top;"><code>audio/ogg</code></td>
   <td style="vertical-align: top;"><code>.oga</code><br>
    <code>.ogg</code></td>
   <td style="vertical-align: top; border-right: 2px solid #d4dde4;">Firefox</td>
   <td style="vertical-align: top;"><code>video/ogg</code></td>
   <td style="vertical-align: top;"><code>.ogv</code><br>
    <code>.ogg</code></td>
   <td style="vertical-align: top;">Firefox</td>
  </tr>
  <tr>
   <th scope="row" style="vertical-align: top;">QuickTime Movie (MOV)</th>
   <td style="vertical-align: top;">—</td>
   <td style="vertical-align: top;">—</td>
   <td style="vertical-align: top; border-right: 2px solid #d4dde4;">—</td>
   <td style="vertical-align: top;"><code>video/quicktime</code></td>
   <td style="vertical-align: top;"><code>.mov</code></td>
   <td style="vertical-align: top;">Safari</td>
  </tr>
  <tr>
   <th scope="row" style="vertical-align: top;">WAV (Waveform Audiofile)</th>
   <td style="vertical-align: top;"><code>audio/wav</code></td>
   <td style="vertical-align: top;"><code>.wav</code></td>
   <td style="vertical-align: top; border-right: 2px solid #d4dde4;">Firefox</td>
   <td style="vertical-align: top;">—</td>
   <td style="vertical-align: top;">—</td>
   <td style="vertical-align: top;">—</td>
  </tr>
  <tr>
   <th scope="row" style="vertical-align: top;">WebM</th>
   <td style="vertical-align: top;"><code>audio/webm</code></td>
   <td style="vertical-align: top;"><code>.webm</code></td>
   <td style="vertical-align: top; border-right: 2px solid #d4dde4;">Firefox</td>
   <td style="vertical-align: top;"><code>video/webm</code></td>
   <td style="vertical-align: top;"><code>.webm</code></td>
   <td style="vertical-align: top;">Firefox</td>
  </tr>
 </tbody>
</table>

<h2 id="See_also">See also</h2>

<ul>
 <li><a href="/en-US/docs/Web/API/WebRTC_API">WebRTC API</a></li>
 <li><a href="/en-US/docs/Web/API/MediaStream_Recording_API">MediaStream Recording API</a></li>
 <li>{{HTMLElement("audio")}} and {{HTMLElement("video")}} elements</li>
</ul>