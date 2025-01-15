# Notes

notes regarding the
[model course repository](https://github.com/cslmath/model-Courses).

```bash
# Copy all tracked model course files from the live location to the staging location
cd model-Courses
rsync -avv --include-from=model-include-from --exclude-from=model-exclude-from /opt/webwork/courses/* ./

# Copy all tracked model course files from the staging location into the live location
sudo rsync -avv --include-from=model-include-from --exclude-from=model-exclude-from ./* /opt/webwork/courses/
sudo chown -R www-data:www-data /opt/webwork/courses/

# Update staging from GitHub
git pull

# Update GitHub from staging
git push

# Create a new model course from an existing model course,
# keeping all git history intact in both courses

# create the new course, properly named <new-model>,
# from <old-model> in the web interface

# to properly preserve the edit history of both models in git:

git checkout -b dup
git mv <old-model> <new-model>
git commit -m "Duplicate <old-model> <new-model>"

# optional
# rsync
# git status
# etc
# but caution, with any extra commits, the following command needs additional ~'s

git checkout HEAD~ <old-model>
git commit -m "Restore <old-model>"

git checkout -
git merge --no-ff dup

# merge new <new-model> into main

# when all is done
git branch -d dup
```

The model course naming scheme:
    modelDDD-CCC
    where DDD is the discipline number (201) and CCC is the course short reference.
    example: `model201-NYB`

The course title can have more detail if needed, for example,
_model201-SN3 Calculus II: Integral Calculus for Science)_.
