---
switcher-label: Imports
---

# Filesystem

API support and documentation for the `node:fs` and `node:fs/promises` modules.

<tldr>
    <p>Modules: <code>node:fs</code>, <code>node:fs/promises</code></p>
    <p>Support: <img style="inline" src="https://img.shields.io/badge/-alpha-blue" /></p>
    <p>Docs: <a href="https://nodejs.org/api/fs.html">Node.js Filesystem Docs</a></p>
</tldr>

<code-block lang="javascript" switcher-key="ESM">import fs from "node:fs"</code-block>
<code-block lang="javascript" switcher-key="CJS">const fs = require("node:fs")</code-block>
<code-block lang="javascript" switcher-key="ESM">import fs from "node:fs/promises"</code-block>
<code-block lang="javascript" switcher-key="CJS">const fs = require("node:fs/promises")</code-block>

## Modules

| Status                  | Module             | Docs                                                                 |
|-------------------------|--------------------|----------------------------------------------------------------------|
| 🟡 Partially supported. | `node:fs`          | [Filesystem](https://nodejs.org/api/fs.html)                         |
| 🟡 Partially supported. | `node:fs/promises` | [Filesystem (Promises)](https://nodejs.org/api/fs.html#promises-api) |

## `fs` | Classes

[`Dir`](https://nodejs.org/api/fs.html#class-fsdir)
: 🔴 Not implemented.

[`Dirent`](https://nodejs.org/api/fs.html#class-fsdirent)
: 🔴 Not implemented.

[`FSWatcher`](https://nodejs.org/api/fs.html#class-fsfswatcher)
: 🔴 Not implemented.

[`StatWatcher`](https://nodejs.org/api/fs.html#class-fsstatwatcher)
: 🔴 Not implemented.

[`ReadStream`](https://nodejs.org/api/fs.html#class-fsreadstream)
: 🔴 Not implemented.

[`Stats`](https://nodejs.org/api/fs.html#class-fsstats)
: 🔴 Not implemented.

[`StatFs`](https://nodejs.org/api/fs.html#class-fsstatfs)
: 🔴 Not implemented.

[`WriteStream`](https://nodejs.org/api/fs.html#class-fswritestream)
: 🔴 Not implemented.

## `fs` | Properties

[`constants`](https://nodejs.org/api/fs.html#fsconstants)
: 🟢 Supported.

## `fs` | Methods

[`access(path[, mode], callback)`](https://nodejs.org/api/fs.html#fsaccesspath-mode-callback)
: 🟢 Supported.

[`accessSync(path[, mode])`](https://nodejs.org/api/fs.html#fsaccesssyncpath-mode)
: 🟢 Supported.

[`appendFile(path, data[, options], callback)`](https://nodejs.org/api/fs.html#fsappendfilepath-data-options-callback)
: 🔴 Not implemented.

[`appendFileSync(path, data[, options])`](https://nodejs.org/api/fs.html#fsappendfilesyncpath-data-options)
: 🔴 Not implemented.

[`chmod(path, mode, callback)`](https://nodejs.org/api/fs.html#fschmodpath-mode-callback)
: 🔴 Not implemented.

[`chmodSync(path, mode)`](https://nodejs.org/api/fs.html#fschmodsyncpath-mode)
: 🔴 Not implemented.

[`chown(path, uid, gid, callback)`](https://nodejs.org/api/fs.html#fschownpath-uid-gid-callback)
: 🔴 Not implemented.

[`chownSync(path, uid, gid)`](https://nodejs.org/api/fs.html#fschownsyncpath-uid-gid)
: 🔴 Not implemented.

[`close(fs[, callback])`](https://nodejs.org/api/fs.html#fsclosefd-callback)
: 🔴 Not implemented.

[`closeSync(fs)`](https://nodejs.org/api/fs.html#fsclosefdsync)
: 🔴 Not implemented.

[`copyFile(src, dest[, mode], callback)`](https://nodejs.org/api/fs.html#fscopyfilesrc-dest-mode-callback)
: 🔴 Not implemented.

[`copyFileSync(src, dest[, mode])`](https://nodejs.org/api/fs.html#fscopyfilesyncsrc-dest-mode)
: 🔴 Not implemented.

[`cp(src, dest[, options], callback)`](https://nodejs.org/api/fs.html#fscpsrc-dest-options-callback)
: 🔴 Not implemented.

[`cpSync(src, dest[, options])`](https://nodejs.org/api/fs.html#fscpsyncsrc-dest-options)
: 🔴 Not implemented.

[`createReadStream(path[, options])`](https://nodejs.org/api/fs.html#fscreatereadstreampath-options)
: 🔴 Not implemented.

[`createWriteStream(path[, options])`](https://nodejs.org/api/fs.html#fscreatewritestreampath-options)
: 🔴 Not implemented.

[`exists(path, callback)`](https://nodejs.org/api/fs.html#fsexistspath-callback)
: 🟢 Supported. Deprecated since Node v1.

[`existsSync(path)`](https://nodejs.org/api/fs.html#fsexistssyncpath)
: 🟢 Supported. Deprecated since Node v1.

[`fchmod(fd, mode, callback)`](https://nodejs.org/api/fs.html#fsfchmodfd-mode-callback)
: 🔴 Not implemented.

[`fchmodSync(fd, mode)`](https://nodejs.org/api/fs.html#fsfchmodsyncfd-mode)
: 🔴 Not implemented.

[`fchown(fd, uid, gid, callback)`](https://nodejs.org/api/fs.html#fsfchownfd-uid-gid-callback)
: 🔴 Not implemented.

[`fchownSync(fd, uid, gid)`](https://nodejs.org/api/fs.html#fsfchownsyncfd-uid-gid)
: 🔴 Not implemented.

[`fdatasync(fd, callback)`](https://nodejs.org/api/fs.html#fsfdatasyncfd-callback)
: 🔴 Not implemented.

[`fdatasyncSync(fd)`](https://nodejs.org/api/fs.html#fsfdatasyncsyncfd)
: 🔴 Not implemented.

[`fstat(fd[, options], callback)`](https://nodejs.org/api/fs.html#fsfstatfd-options-callback)
: 🔴 Not implemented.

[`fstatSync(fd[, options])`](https://nodejs.org/api/fs.html#fsfstatsyncfd-options)
: 🔴 Not implemented.

[`fsync(fd, callback)`](https://nodejs.org/api/fs.html#fsfsyncfd-callback)
: 🔴 Not implemented.

[`fsyncSync(fd)`](https://nodejs.org/api/fs.html#fsfsyncsyncfd)
: 🔴 Not implemented.

[`ftruncate(fd[, len], callback)`](https://nodejs.org/api/fs.html#fsftruncatefd-len-callback)
: 🔴 Not implemented.

[`ftruncateSync(fd[, len])`](https://nodejs.org/api/fs.html#fsftruncatesyncfd-len)
: 🔴 Not implemented.

[`futimes(fd, atime, mtime, callback)`](https://nodejs.org/api/fs.html#fsfutimesfd-atime-mtime-callback)
: 🔴 Not implemented.

[`futimesSync(fd, atime, mtime)`](https://nodejs.org/api/fs.html#fsfutimessyncfd-atime-mtime)
: 🔴 Not implemented.

[`glob(pattern[, options], callback)`](https://nodejs.org/api/fs.html#fsglobpattern-options-callback)
: 🔴 Not implemented.

[`globSync(pattern[, options])`](https://nodejs.org/api/fs.html#fsglobsyncpattern-options)
: 🔴 Not implemented.

[`lchmod(path, mode, callback)`](https://nodejs.org/api/fs.html#fslchmodpath-mode-callback)
: 🔴 Not implemented.

[`lchmodSync(path, mode)`](https://nodejs.org/api/fs.html#fslchmodsyncpath-mode)
: 🔴 Not implemented.

[`lchown(path, uid, gid, callback)`](https://nodejs.org/api/fs.html#fslchownpath-uid-gid-callback)
: 🔴 Not implemented.

[`lchownSync(path, uid, gid)`](https://nodejs.org/api/fs.html#fslchownsyncpath-uid-gid)
: 🔴 Not implemented.

[`lutimes(path, atime, mtime, callback)`](https://nodejs.org/api/fs.html#fslutimespath-atime-mtime-callback)
: 🔴 Not implemented.

[`lutimesSync(path, atime, mtime)`](https://nodejs.org/api/fs.html#fslutimessyncpath-atime-mtime)
: 🔴 Not implemented.

[`link(existingPath, newPath, callback)`](https://nodejs.org/api/fs.html#fslinkexistingpath-newpath-callback)
: 🔴 Not implemented.

[`linkSync(existingPath, newPath)`](https://nodejs.org/api/fs.html#fslinksyncexistingpath-newpath)
: 🔴 Not implemented.

[`lstat(path[, options], callback)`](https://nodejs.org/api/fs.html#fslstatpath-options-callback)
: 🔴 Not implemented.

[`lstatSync(path[, options])`](https://nodejs.org/api/fs.html#fslstatsyncpath-options)
: 🔴 Not implemented.

[`mkdir(path[, options], callback)`](https://nodejs.org/api/fs.html#fsmkdirpath-options-callback)
: 🟢 Supported.

[`mkdirSync(path[, options])`](https://nodejs.org/api/fs.html#fsmkdirsyncpath-options)
: 🟢 Supported.

[`mkdtemp(prefix[, options], callback)`](https://nodejs.org/api/fs.html#fsmkdtempprefix-options-callback)
: 🔴 Not implemented.

[`mkdtempSync(prefix[, options])`](https://nodejs.org/api/fs.html#fsmkdtempsyncprefix-options)
: 🔴 Not implemented.

[`open(path[, flags[, mode]], callback)`](https://nodejs.org/api/fs.html#fsopenpath-flags-mode-callback)
: 🔴 Not implemented.

[`openSync(path[, flags[, mode]])`](https://nodejs.org/api/fs.html#fsopensyncpath-flags-mode)
: 🔴 Not implemented.

[`openAsBlob(path[, options])`](https://nodejs.org/api/fs.html#fsopenasblobpath-options)
: 🔴 Not implemented.

[`opendir(path[, options], callback)`](https://nodejs.org/api/fs.html#fsopendirpath-options-callback)
: 🔴 Not implemented.

[`opendirSync(path[, options])`](https://nodejs.org/api/fs.html#fsopendirsyncpath-options)
: 🔴 Not implemented.

[`read(fd, buffer, offset, length, position, callback)`](https://nodejs.org/api/fs.html#fsreadfd-buffer-offset-length-position-callback)
: 🔴 Not implemented.

[`readSync(fd, buffer, offset, length, position)`](https://nodejs.org/api/fs.html#fsreadsyncfd-buffer-offset-length-position)
: 🔴 Not implemented.

[`read(fd[, options], callback)`](https://nodejs.org/api/fs.html#fsreadfd-options-callback)
: 🔴 Not implemented.

[`readSync(fd[, options])`](https://nodejs.org/api/fs.html#fsreadsyncfd-options)
: 🔴 Not implemented.

[`read(fd, buffer[, options], callback)`](https://nodejs.org/api/fs.html#fsreadfd-buffer-options-callback)
: 🔴 Not implemented.

[`readSync(fd, buffer[, options])`](https://nodejs.org/api/fs.html#fsreadsyncfd-buffer-options)
: 🔴 Not implemented.

[`readdir(path[, options], callback)`](https://nodejs.org/api/fs.html#fsreaddirpath-options-callback)
: 🔴 Not implemented.

[`readdirSync(path[, options])`](https://nodejs.org/api/fs.html#fsreaddirsyncpath-options)
: 🔴 Not implemented.

[`readFile(path[, options], callback)`](https://nodejs.org/api/fs.html#fsreadfilepath-options-callback)
: 🟡 Supported for UTF-8 reads. Binary reads do not work yet.

[`readFileSync(path[, options])`](https://nodejs.org/api/fs.html#fsreadfilesyncpath-options)
: 🟡 Supported for UTF-8 reads. Binary reads do not work yet.

[`readlink(path[, options], callback)`](https://nodejs.org/api/fs.html#fsreadlinkpath-options-callback)
: 🔴 Not implemented.

[`readlinkSync(path[, options])`](https://nodejs.org/api/fs.html#fsreadlinksyncpath-options)
: 🔴 Not implemented.

[`readv(fd, buffers[, position], callback)`](https://nodejs.org/api/fs.html#fsreadvfd-buffers-position-callback)
: 🔴 Not implemented.

[`readvSync(fd, buffers[, position])`](https://nodejs.org/api/fs.html#fsreadvsyncfd-buffers-position)
: 🔴 Not implemented.

[`readv(fd, buffers[, position], callback)`](https://nodejs.org/api/fs.html#fsreadvfd-buffers-position-callback)
: 🔴 Not implemented.

[`readvSync(fd, buffers[, position])`](https://nodejs.org/api/fs.html#fsreadvsyncfd-buffers-position)
: 🔴 Not implemented.

[`realpath(path[, options], callback)`](https://nodejs.org/api/fs.html#fsrealpathpath-options-callback)
: 🔴 Not implemented.

[`realpathSync(path[, options], callback)`](https://nodejs.org/api/fs.html#fsrealpathsyncpath-options)
: 🔴 Not implemented.

[`realpath.native(path[, options], callback)`](https://nodejs.org/api/fs.html#fsrealpathnativepath-options-callback)
: 🔴 Not implemented.

[`realpathSync.native(path[, options], callback)`](https://nodejs.org/api/fs.html#fsrealpathsyncnativepath-options)
: 🔴 Not implemented.

[`rename(oldPath, newPath, callback)`](https://nodejs.org/api/fs.html#fsrenameoldpath-newpath-callback)
: 🔴 Not implemented.

[`renameSync(oldPath, newPath)`](https://nodejs.org/api/fs.html#fsrenamesyncoldpath-newpath)
: 🔴 Not implemented.

[`rmdir(path[, options], callback)`](https://nodejs.org/api/fs.html#fsrmdirpath-options-callback)
: 🔴 Not implemented.

[`rmdirSync(path[, options])`](https://nodejs.org/api/fs.html#fsrmdirsyncpath-options)
: 🔴 Not implemented.

[`rm(path[, options], callback)`](https://nodejs.org/api/fs.html#fsrmpath-options-callback)
: 🔴 Not implemented.

[`rmSync(path[, options])`](https://nodejs.org/api/fs.html#fsrmsyncpath-options)
: 🔴 Not implemented.

[`stat(path[, options], callback)`](https://nodejs.org/api/fs.html#fsstatpath-options-callback)
: 🔴 Not implemented.

[`statSync(path[, options])`](https://nodejs.org/api/fs.html#fsstatsyncpath-options)
: 🔴 Not implemented.

[`statfs(path[, options], callback)`](https://nodejs.org/api/fs.html#fsstatfspath-options-callback)
: 🔴 Not implemented.

[`statfsSync(path[, options])`](https://nodejs.org/api/fs.html#fsstatfssyncpath-options)
: 🔴 Not implemented.

[`symlink(target, path[, type], callback)`](https://nodejs.org/api/fs.html#fssymlinktarget-path-type-callback)
: 🔴 Not implemented.

[`symlinkSync(target, path[, type])`](https://nodejs.org/api/fs.html#fssymlinksynctarget-path-type)
: 🔴 Not implemented.

[`truncate(path[, len], callback)`](https://nodejs.org/api/fs.html#fstruncatepath-len-callback)
: 🔴 Not implemented.

[`truncateSync(path[, len])`](https://nodejs.org/api/fs.html#fstruncatesyncpath-len)
: 🔴 Not implemented.

[`unlink(path, callback)`](https://nodejs.org/api/fs.html#fsunlinkpath-callback)
: 🔴 Not implemented.

[`unlinkSync(path)`](https://nodejs.org/api/fs.html#fsunlinksyncpath)
: 🔴 Not implemented.

[`unwatchFile(filename[, listener])`](https://nodejs.org/api/fs.html#fsunwatchfilefilename-listener)
: 🔴 Not implemented.

[`utimes(path, atime, mtime, callback)`](https://nodejs.org/api/fs.html#fsutimespath-atime-mtime-callback)
: 🔴 Not implemented.

[`utimesSync(path, atime, mtime)`](https://nodejs.org/api/fs.html#fsutimessyncpath-atime-mtime)
: 🔴 Not implemented.

[`watch(filename[, options][, listener])`](https://nodejs.org/api/fs.html#fswatchfilename-options-listener)
: 🔴 Not implemented.

[`watchFile(filename[, options][, listener])`](https://nodejs.org/api/fs.html#fswatchfilefilename-options-listener)
: 🔴 Not implemented.

[`write(fd, buffer, offset[, length[, position]], callback)`](https://nodejs.org/api/fs.html#fswritefd-buffer-offset-length-position-callback)
: 🔴 Not implemented.

[`writeSync(fd, buffer, offset[, length[, position]])`](https://nodejs.org/api/fs.html#fswritesyncfd-buffer-offset-length-position)
: 🔴 Not implemented.

[`write(fd, buffer[, options], callback)`](https://nodejs.org/api/fs.html#fswritefd-buffer-options-callback)
: 🔴 Not implemented.

[`writeSync(fd, buffer[, options])`](https://nodejs.org/api/fs.html#fswritesyncfd-buffer-options)
: 🔴 Not implemented.

[`write(fd, string[, position[, encoding]], callback)`](https://nodejs.org/api/fs.html#fswritefd-string-position-encoding-callback)
: 🔴 Not implemented.

[`writeSync(fd, string[, position[, encoding]])`](https://nodejs.org/api/fs.html#fswritesyncfd-string-position-encoding)
: 🔴 Not implemented.

[`writeFile(file, data[, options], callback)`](https://nodejs.org/api/fs.html#fswritefilefile-data-options-callback)
: 🟡 Supported. `Buffer` cannot be used for writes yet.

[`writeFileSync(file, data[, options])`](https://nodejs.org/api/fs.html#fswritefilesyncfile-data-options)
: 🟡 Supported. `Buffer` cannot be used for writes yet.

[`writev(fd, buffers[, position], callback)`](https://nodejs.org/api/fs.html#fswritevfd-buffers-position-callback)
: 🔴 Not implemented.

[`writevSync(fd, buffers[, position])`](https://nodejs.org/api/fs.html#fswritevsyncfd-buffers-position)
: 🔴 Not implemented.

## `fs/promises` | Classes

[`FileHandle`](https://nodejs.org/api/fs.html#class-filehandle)
: 🔴 Not implemented.

## `fs/promises` | Properties

[`constants`](https://nodejs.org/api/fs.html#fspromisesconstants)
: 🟢 Supported.

## `fs/promises` | Methods

[`access(path[, mode])`](https://nodejs.org/api/fs.html#fspromisesaccesspath-mode)
: 🔴 Not implemented.

[`appendFile(path, data[, options])`](https://nodejs.org/api/fs.html#fspromisesappendfilepath-data-options)
: 🔴 Not implemented.

[`chmod(path, mode)`](https://nodejs.org/api/fs.html#fspromiseschmodpath-mode)
: 🔴 Not implemented.

[`chown(path, uid, gid)`](https://nodejs.org/api/fs.html#fspromiseschownpath-uid-gid)
: 🔴 Not implemented.

[`copyFile(src, dest[, mode])`](https://nodejs.org/api/fs.html#fspromisescopyfilesrc-dest-mode)
: 🔴 Not implemented.

[`cp(src, dest[, options])`](https://nodejs.org/api/fs.html#fspromisescpsrc-dest-options)
: 🔴 Not implemented.

[`glob(pattern[, options])`](https://nodejs.org/api/fs.html#fspromisesglobpattern-options)
: 🔴 Not implemented.

[`lchmod(path, mode)`](https://nodejs.org/api/fs.html#fspromiseslchmodpath-mode)
: 🔴 Not implemented.

[`lchown(path, uid, gid)`](https://nodejs.org/api/fs.html#fspromiseslchownpath-uid-gid)
: 🔴 Not implemented.

[`luntimes(path, atime, mtime)`](https://nodejs.org/api/fs.html#fspromiseslutimespath-atime-mtime)
: 🔴 Not implemented.

[`link(existingPath, newPath)`](https://nodejs.org/api/fs.html#fspromiseslinkexistingpath-newpath)
: 🔴 Not implemented.

[`lstat(path[, options])`](https://nodejs.org/api/fs.html#fspromiseslstatpath-options)
: 🔴 Not implemented.

[`mkdir(path[, options])`](https://nodejs.org/api/fs.html#fspromisesmkdirpath-options)
: 🔴 Not implemented.

[`mkdtemp(prefix[, options])`](https://nodejs.org/api/fs.html#fspromisesmkdtempprefix-options)
: 🔴 Not implemented.

[`open(path, flags[, mode])`](https://nodejs.org/api/fs.html#fspromisesopenpath-flags-mode)
: 🔴 Not implemented.

[`opendir(path[, options])`](https://nodejs.org/api/fs.html#fspromisesopendirpath-options)
: 🔴 Not implemented.

[`readdir(path[, options])`](https://nodejs.org/api/fs.html#fspromisesreaddirpath-options)
: 🔴 Not implemented.

[`readFile(path[, options])`](https://nodejs.org/api/fs.html#fspromisesreadfilepath-options)
: 🟡 Supported for UTF-8 reads. Binary reads do not work yet.

[`readlink(path[, options])`](https://nodejs.org/api/fs.html#fspromisesreadlinkpath-options)
: 🔴 Not implemented.

[`realpath(path[, options])`](https://nodejs.org/api/fs.html#fspromisesrealpathpath-options)
: 🔴 Not implemented.

[`rename(oldPath, newPath)`](https://nodejs.org/api/fs.html#fspromisesrenameoldpath-newpath)
: 🔴 Not implemented.

[`rmdir(path[, options])`](https://nodejs.org/api/fs.html#fspromisesrmdirpath-options)
: 🔴 Not implemented.

[`rm(path[, options])`](https://nodejs.org/api/fs.html#fspromisesrmpath-options)
: 🔴 Not implemented.

[`stat(path[, options])`](https://nodejs.org/api/fs.html#fspromisesstatpath-options)
: 🔴 Not implemented.

[`statfs(path[, options])`](https://nodejs.org/api/fs.html#fspromisesstatfspath-options)
: 🔴 Not implemented.

[`symlink(target, path[, type])`](https://nodejs.org/api/fs.html#fspromisessymlinktarget-path-type)
: 🔴 Not implemented.

[`truncate(path[, len])`](https://nodejs.org/api/fs.html#fspromisestruncatepath-len)
: 🔴 Not implemented.

[`unlink(path)`](https://nodejs.org/api/fs.html#fspromisesunlinkpath)
: 🔴 Not implemented.

[`utimes(path, atime, mtime)`](https://nodejs.org/api/fs.html#fspromisesutimespath-atime-mtime)
: 🔴 Not implemented.

[`watch(filename[, options])`](https://nodejs.org/api/fs.html#fspromiseswatchfilename-options)
: 🔴 Not implemented.

[`writeFile(file, data[, options])`](https://nodejs.org/api/fs.html#fspromiseswritefilefile-data-options)
: 🔴 Not implemented.
