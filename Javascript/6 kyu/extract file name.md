```javascript
class FileNameExtractor {
    static extractFileName (dirtyFileName) {
        let a = dirtyFileName.split('.') ;
        a.splice(a.length-1);
        a = a.join('.');
        a = a.split('_');
        a.splice(0,1);    
        return a.join('_');
    }
}
```