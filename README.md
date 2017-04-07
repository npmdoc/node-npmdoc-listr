# api documentation for  [listr (v0.11.0)](https://github.com/samverschueren/listr#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-listr.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-listr) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-listr.svg)](https://travis-ci.org/npmdoc/node-npmdoc-listr)
#### Terminal task list

[![NPM](https://nodei.co/npm/listr.png?downloads=true)](https://www.npmjs.com/package/listr)

[![apidoc](https://npmdoc.github.io/node-npmdoc-listr/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-listr_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-listr/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-listr/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-listr/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Sam Verschueren",
        "email": "sam.verschueren@gmail.com",
        "url": "github.com/SamVerschueren"
    },
    "bugs": {
        "url": "https://github.com/samverschueren/listr/issues"
    },
    "dependencies": {
        "chalk": "^1.1.3",
        "cli-truncate": "^0.2.1",
        "figures": "^1.7.0",
        "indent-string": "^2.1.0",
        "is-promise": "^2.1.0",
        "is-stream": "^1.1.0",
        "listr-silent-renderer": "^1.1.1",
        "listr-update-renderer": "^0.2.0",
        "listr-verbose-renderer": "^0.4.0",
        "log-symbols": "^1.0.2",
        "log-update": "^1.0.2",
        "ora": "^0.2.3",
        "rxjs": "^5.0.0-beta.11",
        "stream-to-observable": "^0.1.0",
        "strip-ansi": "^3.0.1"
    },
    "description": "Terminal task list",
    "devDependencies": {
        "ava": "*",
        "clinton": "*",
        "coveralls": "^2.11.14",
        "delay": "^1.3.1",
        "hook-std": "^0.2.0",
        "nyc": "^8.3.2",
        "xo": "*",
        "zen-observable": "^0.3.0"
    },
    "directories": {},
    "dist": {
        "shasum": "5e778bc23806ac3ab984ed75564458151f39b03e",
        "tarball": "https://registry.npmjs.org/listr/-/listr-0.11.0.tgz"
    },
    "engines": {
        "node": ">=4"
    },
    "files": [
        "index.js",
        "lib"
    ],
    "gitHead": "7b334b155a06100d1614b78eaba9220e063bdec0",
    "homepage": "https://github.com/samverschueren/listr#readme",
    "keywords": [
        "cli",
        "task",
        "list",
        "tasklist",
        "terminal",
        "term",
        "console",
        "ascii",
        "unicode",
        "loading",
        "indicator",
        "progress",
        "busy",
        "wait",
        "idle"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "samverschueren",
            "email": "sam.verschueren@gmail.com"
        }
    ],
    "name": "listr",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/samverschueren/listr.git"
    },
    "scripts": {
        "coveralls": "nyc report --reporter=text-lcov | coveralls",
        "test": "clinton && xo && nyc ava"
    },
    "version": "0.11.0",
    "xo": {
        "esnext": true
    }
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module listr](#apidoc.module.listr)
1.  object <span class="apidocSignatureSpan">listr.</span>renderer
1.  object <span class="apidocSignatureSpan">listr.</span>state
1.  object <span class="apidocSignatureSpan">listr.</span>utils

#### [module listr.renderer](#apidoc.module.listr.renderer)
1.  [function <span class="apidocSignatureSpan">listr.renderer.</span>getRenderer (renderer, fallbackRenderer)](#apidoc.element.listr.renderer.getRenderer)

#### [module listr.state](#apidoc.module.listr.state)
1.  [function <span class="apidocSignatureSpan">listr.state.</span>toString (input)](#apidoc.element.listr.state.toString)
1.  number <span class="apidocSignatureSpan">listr.state.</span>COMPLETED
1.  number <span class="apidocSignatureSpan">listr.state.</span>FAILED
1.  number <span class="apidocSignatureSpan">listr.state.</span>PENDING
1.  number <span class="apidocSignatureSpan">listr.state.</span>SKIPPED

#### [module listr.utils](#apidoc.module.listr.utils)
1.  [function <span class="apidocSignatureSpan">listr.utils.</span>isListr (obj && obj.setRenderer && obj.add && obj.run)](#apidoc.element.listr.utils.isListr)
1.  [function <span class="apidocSignatureSpan">listr.utils.</span>isObservable (obj && typeof obj.subscribe === 'function' && obj.constructor.name === 'Observable')](#apidoc.element.listr.utils.isObservable)



# <a name="apidoc.module.listr"></a>[module listr](#apidoc.module.listr)



# <a name="apidoc.module.listr.renderer"></a>[module listr.renderer](#apidoc.module.listr.renderer)

#### <a name="apidoc.element.listr.renderer.getRenderer"></a>[function <span class="apidocSignatureSpan">listr.renderer.</span>getRenderer (renderer, fallbackRenderer)](#apidoc.element.listr.renderer.getRenderer)
- description and source-code
```javascript
(renderer, fallbackRenderer) => {
	let ret = getRendererClass(renderer);

	if (!isRendererSupported(ret)) {
		ret = getRendererClass(fallbackRenderer);

		if (!ret || !isRendererSupported(ret)) {
			ret = renderers.verbose;
		}
	}

	return ret;
}
```
- example usage
```shell
...
		this._options = Object.assign({
			showSubtasks: true,
			concurrent: false,
			renderer: 'default',
			nonTTYRenderer: 'verbose'
		}, opts);
		this._tasks = [];
		this._RendererClass = renderer.getRenderer(this._options.renderer, this._options.nonTTYRenderer);

		this.exitOnError = this._options.exitOnError;

		this.add(tasks || []);
	}

	_checkAll(context) {
...
```



# <a name="apidoc.module.listr.state"></a>[module listr.state](#apidoc.module.listr.state)

#### <a name="apidoc.element.listr.state.toString"></a>[function <span class="apidocSignatureSpan">listr.state.</span>toString (input)](#apidoc.element.listr.state.toString)
- description and source-code
```javascript
input => {
	switch (input) {
		case state.PENDING:
			return 'pending';
		case state.COMPLETED:
			return 'completed';
		case state.FAILED:
			return 'failed';
		case state.SKIPPED:
			return 'skipped';
		default:
			return 'unknown';
	}
}
```
- example usage
```shell
...

		this.next({
			type: 'STATE'
		});
	}

	get state() {
		return state.toString(this._state);
	}

	check(ctx) {
		// Check if a task is enabled or disabled
		if (this._state === undefined && this._enabledFn) {
			const isEnabled = this._enabledFn(ctx);
...
```



# <a name="apidoc.module.listr.utils"></a>[module listr.utils](#apidoc.module.listr.utils)

#### <a name="apidoc.element.listr.utils.isListr"></a>[function <span class="apidocSignatureSpan">listr.utils.</span>isListr (obj && obj.setRenderer && obj.add && obj.run)](#apidoc.element.listr.utils.isListr)
- description and source-code
```javascript
obj => Boolean(obj && obj.setRenderer && obj.add && obj.run)
```
- example usage
```shell
...
	hasFailed() {
		return this._state === state.FAILED;
	}

	run(context, wrapper) {
		const handleResult = result => {
			// Detect the subtask
			if (utils.isListr(result)) {
				result._options = Object.assign(this._options, result._options);

				result.exitOnError = result._options.exitOnError;

				result.setRenderer(renderer.getRenderer('silent'));
				this._subtasks = result.tasks;
...
```

#### <a name="apidoc.element.listr.utils.isObservable"></a>[function <span class="apidocSignatureSpan">listr.utils.</span>isObservable (obj && typeof obj.subscribe === 'function' && obj.constructor.name === 'Observable')](#apidoc.element.listr.utils.isObservable)
- description and source-code
```javascript
obj => Boolean(obj && typeof obj.subscribe === 'function' && obj.constructor.name === 'Observable')
```
- example usage
```shell
...

			// Detect stream
			if (isStream(result)) {
				result = streamToObservable(result);
			}

			// Detect Observable
			if (utils.isObservable(result)) {
				result = new Promise((resolve, reject) => {
					result.subscribe({
						next: data => {
							this._output = data;

							this.next({
								type: 'DATA',
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
