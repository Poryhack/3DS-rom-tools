# Nintendo 3DS ROM Tools
Tools and guides for working with Nintendo 3DS games and applications (.3ds, .cci, .app, .cxi, .cfa, .cia)

There exist some work-in-progress guides at this repository's Wiki: https://github.com/ihaveamac/3DS-rom-tools/wiki

See this list of other tools that might be useful: https://github.com/ihaveamac/3DS-rom-tools/wiki/List-of-useful-tools

## NCCHInfo generation - `/ncchinfo_gen`
* `ncchinfo_gen.py` - Generates `ncchinfo.bin`, which will generate XORpads for a game's ExHeader/ExeFS/RomFS on a 3DS console ([original source](https://github.com/d0k3/Decrypt9WIP/blob/2935c881f436cc940f44a9455c2ae63aff1744d8/scripts/ncchinfo_gen.py))
* `ncchinfo_gen_exh.py` - Generates `ncchinfo.bin` which will only generate XORpads for a ROM's ExHeader and ExeFS

## RSF generation - `/rsfgen`
* `rsfgen.py` - Generates a .rsf, using a .3ds/.cci, decrypted ExHeader, and a template RSF ([original source](https://gbatemp.net/threads/release-exinjector-inject-original-exheaders-into-repacked-roms.373839/page-16#post-5298180))
* `rsfgen_cia.py` - Modified rsfgen, generates a .rsf, using a decrypted CIA and a template RSF
* `rsfgen_exh.py` - Modified rsfgen, generates a .rsf only using decrypted ExHeader and a template RSF; does not automatically get CompanyCode, ProductCode, or UniqueId
* `dummy.rsf` - Template RSF for use with rsfgen; must have DOS line endings (CR LF, try unix2dos if your generated rsf looks strange) ([original source](https://gist.github.com/mid-kid/d9c4ce50407c71ec9ef3))
* `dummy.rsf.zip` - Archived-form of `dummy.rsf`, as an easy way to download this file with the proper line endings

## Downloading - `/downloading`
* `TitleDownloader.py` - download update files from Nintendo CDN; requires [make_cdn_cia](https://github.com/ihaveamac/ctr_toolkit/tree/master/make_cdn_cia) in the user's PATH ([original source](https://gist.github.com/meowy/793cf60a632f8d29e38b))

## Seed database - `/seeddb`
* `seeddb.bin` - contains seeds for games using seed crypto introduced in 9.6.0-24
 * [List of games and title IDs that use seed crypto](https://github.com/ihaveamac/3DS-rom-tools/wiki/SeedDB-list)
