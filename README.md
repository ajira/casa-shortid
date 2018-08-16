Refer [ORIG-README.md](ORIG-README.md) on actual documentation.  

Forked from [shortid](https://github.com/dylang/shortid.git). 

Reason for fork:
1. have a shorter id length (6 instead of 9 as of 16-Aug-2018) 

to achieve this we have to edit `lib\build.js`


> // Ignore all milliseconds before a certain time to reduce the size of the date entropy without sacrificing uniqueness.
> // This number should be updated every year or so to keep the generated id short.
> // To regenerate `new Date() - 0` and bump the version. Always bump the version!
> var REDUCE_TIME = 1459707606518;

1. setting `REDUCE_TIME`  to a recent time
2. setting `version` to 1. Not bumping, as it's forked. 
