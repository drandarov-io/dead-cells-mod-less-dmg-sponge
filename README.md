# Changes 

## Bosses
- 50% HP
- No Damage Cap

# Workflow (notes for myself):
.\PAKTool.exe -Expand -OutDir "export" -RefPak "..\res.pak"
.\CDBTool.exe -Expand -OutDir ".\data.cdb_" -RefCDB "export\data.cdb"

## Make changes

.\CDBTool.exe -Collapse -InDir ".\data.cdb_" -OutCDB "export\data.cdb"
.\PAKTool.exe -CreateDiffPak -RefPak "..\res.pak" -InDir "W:\Games\SteamLibrary\steamapps\common\Dead Cells\ModTools\export" -OutPak ".\mod\res.pak"

## Testing
.\PAKTool.exe -Expand -OutDir "mod\test" -RefPak "mod\res.pak"