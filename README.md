# Support Class' tsconfigs

> Our re-usable TypeScript compiler configurations.

## Usage

1. Install the config(s) you wish to use as devDependencies:

    ```bash
    npm i -D @supportclass/tsconfig-base
    npm i -D @supportclass/tsconfig-nodecg-server
    npm i -D @supportclass/tsconfig-nodecg-client
    ```

2. Copy this boilerplate and save it as your project's `tsconfig.json`.

    ```json
    {
        // Can also be tsconfig-nodecg-server or tsconfig-nodecg-client
        "extends": "@supportclass/tsconfig-base",
        
        "compilerOptions": {
            "rootDir": "src",
            "outDir": "dist",
            "baseUrl": "./",
            "paths": {
                "*": [
                    "./node_modules/*",
                    "./src/types/*"
                ]
            }
        },
        "include": ["src/**/*.ts"],
        "exclude": ["src/**/*spec.ts"]
    }
    ```
    
3. Modify the boilerplate as-needed to fit your project's structure and unique needs.


## Additional Boilerplate

### Polymer 2

Polymer 2 projects may also need this additional boilerplate configuration added to their `tsconfig.json`:

```json
{
	"include": [
		"../../types/browser.d.ts",
		"bower_components/**/*.d.ts",
		"dashboard/**/*.ts",
		"graphics/**/*.ts",
		"shared/**/*.ts"
	]
}
```