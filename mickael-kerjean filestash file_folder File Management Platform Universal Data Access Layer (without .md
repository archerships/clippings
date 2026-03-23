# mickael-kerjean/filestash: :file_folder: File Management Platform / Universal Data Access Layer (without FUSE)
[mickael-kerjean/filestash: :file_folder: File Management Platform / Universal Data Access Layer (without FUSE)](https://github.com/mickael-kerjean/filestash) 

 [![](https://raw.githubusercontent.com/mickael-kerjean/filestash_images/master/.assets/photo.jpg)
](https://raw.githubusercontent.com/mickael-kerjean/filestash_images/master/.assets/photo.jpg)

It started as a storage agnostic Dropbox-like file manager that works with every storage protocol: [FTP](https://www.filestash.app/ftp-client.html), [SFTP](https://www.filestash.app/ssh-file-transfer.html), [S3](https://www.filestash.app/s3-browser.html), [SMB](https://www.filestash.app/smb-client.html), [WebDAV](https://www.filestash.app/webdav-client.html), IPFS, and [about 20 more](https://www.filestash.app/docs/plugin/#storage).

It grew into what we want to be the world's best file management platform, where everything that's not a fundamental truth of the universe lives in a plugin. Where other platforms are take-it-or-leave-it, ours gives you a rock solid core and a plugin system to handle opinions, so however deep requirements go, the only limit won't be technical but your own creativity.

[![](https://camo.githubusercontent.com/43cf77d45929c4cef2abc9a6eb73dcddb5f97a6fe636872da59812cedc156390/68747470733a2f2f7777772e66696c6573746173682e6170702f696d672f696c6c757374726174696f6e2f66696c6573746173682d696e746567726174696f6e732e706e67)
](http://demo.filestash.app/)

*   [Plugin Driven Architecture](#vision--philosophy): everything that matters is a plugin, browse the [ecosystem](https://www.filestash.app/docs/plugin/) or [build your own](https://www.filestash.app/docs/guide/plugin-development.html?origin=github). With this approach, you get exactly what you need without any kind of overhead or bloat.
*   Universal Access: a sleek web client made in vanilla JS that's infinitely customizable via [dynamic patch plugins](https://www.filestash.app/docs/guide/plugin-development.html#patch-plugins-in-depth), plus gateways to access your data via [SFTP](https://www.filestash.app/docs/guide/sftp-gateway.html?origin=github), [MCP](https://www.filestash.app/docs/guide/mcp-gateway.html?origin=github) or S3, integrations via [APIs](https://www.filestash.app/docs/api/#api) and via web components like this [psd viewer](https://www.filestash.app/tools/psd-viewer.html)
*   [Integrations](https://www.filestash.app/docs/plugin/#storage): our explicit goal is to support 100% of storage and authentication technologies on the market. Beyond your usual options, you can go much further, like a [virtual filesystem](https://www.filestash.app/docs/guide/virtual-filesystem.html?origin=github) delegating authentication to your [WordPress site](https://github.com/mickael-kerjean/filestash/tree/master/server/plugin/plg_authenticate_wordpress) and using its roles to drive [RBAC authorization](https://www.filestash.app/docs/guide/authorization.html#option-2-rbac).
*   [Workflow Engine](https://www.filestash.app/docs/guide/workflow-engine.html): automate anything that happens to your files by chaining actions on events, from simple notifications via Slack or email to full on MFT pipelines and everything in between.
*   File Apps: use any of the existing apps or [build your own](https://www.filestash.app/docs/guide/plugin-development.html#xdg-open-plugins-in-depth), from astronomy to embroidery and everything in between like:
    *   [photography](https://demo.filestash.app/assets/plugin/application_photography.zip): heif, nef, raf, [tiff](https://www.filestash.app/tools/tiff-viewer.html), raw, arw, sr2, srf, nrw, cr2, crw, x3f, pef, rw2, orf, mrw, mdc, mef, mos, dcr, kdc, 3fr, erf and srw
    *   [astronomy](https://demo.filestash.app/assets/plugin/application_photography.zip): [fits](https://www.filestash.app/tools/fits-viewer.html), [xisf](https://www.filestash.app/tools/xisf-viewer.html)
    *   [science](https://demo.filestash.app/assets/plugin/application_science.zip): with latex, plantuml & pandoc compilers
    *   [music](https://demo.filestash.app/assets/plugin/application_musician.zip): mid, midi, gp4 and gp5
    *   [GIS](https://demo.filestash.app/assets/plugin/application_gis.zip): [geojson](https://www.filestash.app/tools/geojson-viewer.html), [shp](https://www.filestash.app/tools/shp-viewer.html), gpx, wms and [dbf](https://www.filestash.app/tools/dbf-viewer.html)
    *   [data engineering](https://demo.filestash.app/assets/plugin/application_engineering.zip): [parquet](https://www.filestash.app/tools/parquet-viewer.html), [arrow](https://www.filestash.app/tools/arrow-viewer.html), [feather](https://www.filestash.app/tools/feather-viewer.html), [avro](https://www.filestash.app/tools/avro-viewer.html), [orc](https://www.filestash.app/tools/orc-viewer.html), [hdf5](https://www.filestash.app/tools/hdf5-viewer.html), [h5](https://www.filestash.app/tools/hdf5-viewer.html), [netcdf](https://www.filestash.app/tools/netcdf-viewer.html), [nc](https://www.filestash.app/tools/netcdf-viewer.html), rds, rda and rdata
    *   [dev](https://demo.filestash.app/assets/plugin/application_dev.zip): a, so, o, dylib, dll, tar, tgz, zip, har, cap, pcap, pcapng and [sqlite](https://www.filestash.app/tools/sqlite-viewer.html)
    *   [creative work](https://demo.filestash.app/assets/plugin/application_creative.zip): svg, [psd](https://www.filestash.app/tools/psd-viewer.html), ai, [sketch](https://www.filestash.app/tools/sketch-viewer.html), [cdr](https://www.filestash.app/tools/cdr-viewer.html), woff, woff2, ttf, otf, eot, exr, tga, pgm, ppm, dds, ktx, dpx, pcx, xpm, pnm, xbm, aai, xwd, cin, pbm, pcd, sgi, wbmp and rgb
    *   [biomedical](https://demo.filestash.app/assets/plugin/application_biomed.zip): dicom, sam, bam, cif, pdb, xyz, sdf, mol, mol2 and mmtf
    *   [autodesk](https://demo.filestash.app/assets/plugin/application_autodesk.zip): [dwg](https://www.filestash.app/tools/dwg-viewer.html) and [dxf](https://www.filestash.app/tools/dxf-viewer.html)
    *   [adobe](https://demo.filestash.app/assets/plugin/application_adobe.zip): [psd](https://www.filestash.app/tools/psd-viewer.html), ai, [xd](https://www.filestash.app/tools/xd-viewer.html), [dng](https://www.filestash.app/tools/dng-viewer.html), [postscript](https://www.filestash.app/tools/eps-viewer.html), aco, ase, swf
    *   [3d](https://demo.filestash.app/assets/plugin/application_3d.zip): fbx, gltf, obj, stl, step, mesh, ifc, dae
    *   [embroidery](https://demo.filestash.app/assets/plugin/application_embroidery.zip): dgt, dst, dsb, dsz, edr, exp, 10o, col, hus, inf, jef, ksm, pcm, pcs, pes, sew, shv, sst, tap, u01, vip, vp3 and xxx
    *   [e2e](https://github.com/mickael-kerjean/filestash/tree/master/server/plugin/plg_widget_pgp): pgp, gpg
*   Themes:  
    [![](https://camo.githubusercontent.com/99e82a8bc61206887df5209da4566f46678854863677326783cd6b97f8fe196d/68747470733a2f2f7777772e66696c6573746173682e6170702f696d672f73637265656e73686f74732f7468656d655f6769746875622e706e67)
    ](https://camo.githubusercontent.com/99e82a8bc61206887df5209da4566f46678854863677326783cd6b97f8fe196d/68747470733a2f2f7777772e66696c6573746173682e6170702f696d672f73637265656e73686f74732f7468656d655f6769746875622e706e67) [![](https://camo.githubusercontent.com/05604c39a7f110e30d068f7f6b062dd1493145d86556a1c104cb6e54d641f6d0/68747470733a2f2f7777772e66696c6573746173682e6170702f696d672f73637265656e73686f74732f7468656d655f6170706c652e706e67)
    ](https://camo.githubusercontent.com/05604c39a7f110e30d068f7f6b062dd1493145d86556a1c104cb6e54d641f6d0/68747470733a2f2f7777772e66696c6573746173682e6170702f696d672f73637265656e73686f74732f7468656d655f6170706c652e706e67) [![](https://camo.githubusercontent.com/fe767667706d99599ce45d8b2db1415e39a2e41c818c98e8b8ebc666b422aabb/68747470733a2f2f7777772e66696c6573746173682e6170702f696d672f73637265656e73686f74732f7468656d655f64726f70626f782e706e67)
    ](https://camo.githubusercontent.com/fe767667706d99599ce45d8b2db1415e39a2e41c818c98e8b8ebc666b422aabb/68747470733a2f2f7777772e66696c6573746173682e6170702f696d672f73637265656e73686f74732f7468656d655f64726f70626f782e706e67) [![](https://camo.githubusercontent.com/0f88f036250d8625808fc674d83407db20e9b0cf44937ba9aa540f3c14a6d121/68747470733a2f2f7777772e66696c6573746173682e6170702f696d672f73637265656e73686f74732f7468656d655f69626d2e706e67)
    ](https://camo.githubusercontent.com/0f88f036250d8625808fc674d83407db20e9b0cf44937ba9aa540f3c14a6d121/68747470733a2f2f7777772e66696c6573746173682e6170702f696d672f73637265656e73686f74732f7468656d655f69626d2e706e67)
*   AI features for [search](https://www.filestash.app/docs/guide/search.html), [smart folders](https://www.filestash.app/features/smart-folder.html) and OCRs.
*   ... and much much more (versioning, audit, public site, antivirus, quota, chat, chromecast support, on demand video transcoding, mounting shared links as network drive, ....)  
    As a rule of thumb, if your problem involves files, we either already [have a plugin](https://www.filestash.app/docs/plugin/) for it or can make a plugin for it

To install Filestash, head to the [Getting started](https://www.filestash.app/docs/?origin=github) guide. If you want to leverage plugins, head over to the [inventory](https://www.filestash.app/docs/plugin/?origin=github), or learn about [developing your own plugins](https://www.filestash.app/docs/guide/plugin-development.html?origin=github).

If you want guidance and expert help on your file management problem, [book a call](https://www.filestash.app/tunnel/demo/?origin=github) and let's figure out if Filestash is the right platform for you.

Our goal is simple: **to build the best file management platform ever made. Period.** But "best" means different things to different people, and making Filestash modular is the only sane model to accomplish that. Anything that isn't a fundamental truth of the universe and might spark a debate belongs in a plugin. Literally every piece listed in the key features is a plugin you can swap for another implementation or remove entirely.

This modularity is made possible by the magic of programming interfaces. For example, if you want a [Dropbox-like frontend for FTP](https://news.ycombinator.com/item?id=9224), you will find out the [FTP plugin](https://github.com/mickael-kerjean/filestash/tree/master/server/plugin/plg_backend_ftp) simply implements this interface:

```go
type IBackend interface {
	Ls(path string) ([]os.FileInfo, error)           // list files in a folder
	Stat(path string) (os.FileInfo, error)           // file stat
	Cat(path string) (io.ReadCloser, error)          // download a file
	Mkdir(path string) error                         // create a folder
	Rm(path string) error                            // remove something
	Mv(from string, to string) error                 // rename something
	Save(path string, file io.Reader) error          // save a file
	Touch(path string) error                         // create a file

	// I have omitted 2 other methods, a first one to enable connections reuse and
	// another one to declare what should the login form be like.
}
```

There are interfaces you can implement for every key component of Filestash: from storage, to authentication, [authorisation](https://www.filestash.app/docs/guide/authorization.html), custom apps, [search](https://www.filestash.app/docs/guide/search.html), thumbnailing, frontend patches, middleware, endpoint creation and a few others documented in the [plugin development guide](https://www.filestash.app/docs/guide/plugin-development.html).

To see what's currently installed in your instance, head over to [/about](https://demo.filestash.app/about). The inventory of plugins is [documented here](https://www.filestash.app/docs/plugin/)

*   Commercial Users → [support contract](https://www.filestash.app/pricing/?origin=github)
*   For individuals:
    *   [#filestash](https://kiwiirc.com/nextclient/#irc://irc.libera.chat/#filestash?nick=guest??) on IRC (libera.chat)
    *   Bitcoin: `3LX5KGmSmHDj5EuXrmUvcg77EJxCxmdsgW`
    *   [Open Collective](https://opencollective.com/filestash)

Filestash stands on the shoulder of: [contributors](https://github.com/mickael-kerjean/filestash/graphs/contributors), folks developing [awesome libraries](https://github.com/mickael-kerjean/filestash/blob/master/go.mod), a whole bunch of C stuff (the [C standard library](https://imgs.xkcd.com/comics/dependency.png), [libjpeg](https://libjpeg-turbo.org/), [libpng](https://www.libpng.org/pub/png/libpng.html), [libgif](https://giflib.sourceforge.net/), [libraw](https://www.libraw.org/about) and many more), [fontawesome](https://fontawesome.com/), [material](https://material.io/icons/), [Browser stack](https://www.browserstack.com/) to let us test on real devices, and the many guys from Nebraska and elsewhere who have been thanklessly maintaining the critical pieces that Filestash sits on top:

[![](https://camo.githubusercontent.com/a7e63bf8fe7e3e55bc8ff43860107825410b4ae6c02578e8f361b5a19e80a7df/68747470733a2f2f696d67732e786b63642e636f6d2f636f6d6963732f646570656e64656e63792e706e67)
](https://camo.githubusercontent.com/a7e63bf8fe7e3e55bc8ff43860107825410b4ae6c02578e8f361b5a19e80a7df/68747470733a2f2f696d67732e786b63642e636f6d2f636f6d6963732f646570656e64656e63792e706e67)